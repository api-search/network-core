---
name: Calculated
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/calculated.png
url: https://example.com/apis/calculated.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Calculated
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
  - name: FactSet ETF Profile and Prices API
    description: >-
      Access FactSet-collected profile data and pricing for Exchange Traded
      Funds (ETFs).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/etf-profile-and-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#changelog
      - type: OpenAPI
        data:
          host: api.factset.com
          swagger: '2.0'
          consumes:
            - application/json
          produces:
            - application/json
          paths:
            /factset/etf/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Profile
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                description: >-
                  An ETP can be profiled by defining several common attributes
                  such as issuer, fund description, and benchmark.
                summary: Retrieve basic profile information for a specified ETP.
            /factset/etf/allocation/asset/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Asset
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  asset class. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's asset allocations.
            /factset/etf/allocation/country/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Country
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  country names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's country allocations.
            /factset/etf/allocation/currency/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Currency
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  currency. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's currency allocations.
            /factset/etf/allocation/economicDevelopment/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Economic
                  - Development
                  - Status.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  List of allocations classified by a holding's economic
                  development status (e.g. developed market, frontier market,
                  emerging market).
                summary: >-
                  List of allocations classified by a holding's economic
                  development status.
            /factset/etf/allocation/exchange/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Exchange
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  exchanges. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's exchange allocations.
            /factset/etf/allocation/industry/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Industry
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  industry. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's industry allocations.
            /factset/etf/allocation/marketCapitalization/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Total
                  - Market
                  - Capitalization.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  List of allocations classified by a holding's total market
                  capitalization (e.g. Small Cap, Mid Cap, Large Cap). Response
                  will be sorted by weight in descending order.
                summary: >-
                  List of allocations classified by a holding's total market
                  capitalization.
            /factset/etf/allocation/region/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Region
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  region names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's region allocations.
            /factset/etf/allocation/sector/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Sector
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  sector names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's sector allocations.
            /factset/etf/analytics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Analytics
                  - Datapoints
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet's proprietary analytical datapoints include ETP
                  attributes specific to lending, corporate actions, and
                  benchmarks.
                summary: FactSet proprietary analytics datapoints for ETPs.
            /factset/etf/analytics/holdings/statistics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Portfolio
                  - Statistics
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates several proprietary portfolio statistics
                  for ETPs including average maturity, credit quality,
                  price/book ratio, price/earnings ratio, and dividend yield.
                summary: FactSet's portfolio statistics for ETPs.
            /factset/etf/analytics/score/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Rankings.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates various proprietary fund rankings including
                  unique scores, fund grades, segment averages, and
                  recommendations.
                summary: FactSet proprietary ETP rankings.
            /factset/etf/analytics/trade/getBySymbol:
              get:
                tags:
                  - Trade
                  - Statistics
                  - For
                  - Specific
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  Various metrics of an ETP's liquidity including creation
                  metrics, premium/discount, spread, and tracking error
                  statistics.
                summary: Trade statistics for specific ETP.
            /factset/etf/characteristics/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Characteristic
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  An ETP has many unique characteristics specific to its
                  composition that differentiate it from other products. This
                  includes details on leverage, hedging, derivatives, and
                  service providers.
                summary: Retrieve basic characteristic information for a specified ETP.
            /factset/etf/class/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Classification
                  - Specific
                  - To
                  - Asset
                  - Class,
                  - Geography,
                  - Or
                  - Investment
                  - Strategy.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  ETP classification is divided into three categories: Asset
                  Class, Geography, and Investment Strategy. Asset class is
                  determined based on the various asset types held by the fund,
                  A fund's geography can be classified by region (e.g.
                  Asia-Pac), specific geography (e.g. China) or economic
                  development (e.g. BRIC). An ETP's investment strategy is
                  classified in broad categories (e.g. Large Cap) and more
                  granular categorizations.
                summary: >-
                  Retrieve an ETP's classification specific to asset class,
                  geography, or investment strategy.
            /factset/etf/class/category/broad/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Broad
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                description: List of ETP class broad categories.
                summary: List of ETP class broad categories.
            /factset/etf/class/category/focus/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Focus
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                description: List of ETP class focus categories.
                summary: List of ETP class focus categories.
            /factset/etf/class/category/niche/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Niche
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                description: List of ETP class niche categories.
                summary: List of ETP class niche categories.
            /factset/etf/class/geography/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Geographies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: List of ETP class geographies.
                summary: List of ETP class geographies.
            /factset/etf/competitors/listBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Proprietary
                  - List
                  - Of
                  - Competing
                  - Companies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  FactSet defines and maintains a proprietary list of competing
                  companies based on a number of attributes specific to a fund.
                summary: FactSet's proprietary list of competing companies.
            /factset/etf/distribution/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Current
                  - Distribution
                  - Details.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  Retrieve distribution-related details for a specific ETP
                  including dividend and capital gain distribution details.
                summary: Retrieve an ETP's current distribution details.
            /factset/etf/fundFlows/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Cash
                  - Inflow/outflows
                  - For
                  - Various
                  - Time
                  - Periods.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                description: >-
                  Retrieve the amount invested or divested in a specific ETP
                  over various time periods including one-day, one-week,
                  one-month, one-year, and YTD.
                summary: >-
                  Retrieve an ETP's cash inflow/outflows for various time
                  periods.
            /factset/etf/growthOfTenK/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Growth
                  - Of
                  - '10'
                  - Calculated
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Growth of 10K (or growth of 10,000) is a commonly used chart
                  that highlights the change in the value of an initial 10,000
                  investment in the ETP during a given period of time. Often,
                  this period of time is either since inception or the
                  calculation between the pre-defined range.
                summary: >-
                  This endpoint returns selected ETP's Growth of 10K calculated
                  values.
            /factset/etf/holdings/listBySymbol:
              get:
                tags:
                  - Holdings
                  - Details
                  - For
                  - An
                  - Individual
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Retrieve an ETP's holdings information including security,
                  shares held, and weight.
                summary: Holdings details for an individual ETP.
            /factset/etf/marketAggregates/getBySymbol:
              get:
                tags:
                  - Market
                  - Aggregate
                  - Data
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                description: >-
                  Market Aggregates combines FactSet Estimates, FactSet
                  Fundamentals, and FactSet Prices data to derive ratios and per
                  share values on an aggregate level. The resulting index values
                  can be used to identify market trends and compare a
                  combination of portfolios, benchmarks, and individual
                  securities.
                summary: Market aggregate data for ETPs.
            /factset/etf/premiumDiscount/summary/listBySymbol:
              get:
                tags:
                  - Summary
                  - Of
                  - Premium
                  - Discount
                  - Data.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: Summary of ETP premium discount data.
                summary: Summary of ETP premium discount data.
            /factset/etf/price/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  Retrieve an ETP's historical NAV and shares outstanding for a
                  specified time range.
                summary: Retrieve historical ETP NAV values.
            /factset/etf/returns/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Total
                  - Return
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  An ETP's total return data can be returned for various time
                  frames including 1-month, 3-month, YTD, 1-year, 3-year, and
                  5-year. Total return calculations include price performance
                  plus reinvested and compounded distributions. Market price is
                  used to calcualte market returns. Portfolio nav is used to
                  calcualte nav returns.
                summary: Retrieve total return data for a specified ETP.
            /factset/etf/strategy/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Various
                  - Classification
                  - Details
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  ETP's can be classified in many different ways including
                  investment strategy, security weightings, and fund
                  composition.
                summary: Retrieve various classification details for a specified ETP.
            /factset/etf/strategy/segment/list:
              get:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Strategy
                  - Segments.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve the various segments assigned to a specific ETP.
                  Segment data is used to group funds for comparison and
                  relative performance analyses.
                summary: Retrieve a list of ETP strategy segments.
            /factset/etf/structure/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Basic
                  - Structure
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve details on a fund's structure including its type,
                  investment style (active/passive), and legal structure.
                summary: Retrieve the basic structure information for a specified ETP.
            /factset/etf/taxesAndFees/us/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Tax
                  - And
                  - Fee
                  - Related
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                description: >-
                  Retrieve various fee and tax related details on a specified
                  ETP including expense ratio and tax treatment for dividends
                  and capital gains.
                summary: >-
                  Retrieve the tax and fee related information for a specified
                  ETP.
            /factset/etf/timeSeries/listBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                  - Series
                description: >-
                  Retrieve the historical NAV data and the respective fund flows
                  and shares outstanding for a specified fund and time period.
                  Please refer currency.fund in /factset/etf/getBySymbol for
                  currency value.
                summary: Retrieve historical NAV data for a specified ETP.
          info:
            title: Prime Developer Trial
          x-interface-version: 1
          x-documenter-version: 5.38.1
          x-api-version: 2.9.1
          tags:
            - name: factset
              description: factset endpoints
          responses:
            ErrorResponse:
              description: Generic error response for all errors (400 ... 599 error codes)
              schema:
                type: object
                properties:
                  meta:
                    $ref: '#/definitions/ErrorMetaObject'
                  errors:
                    $ref: '#/definitions/ErrorObject'
          definitions:
            ErrorMetaObject:
              type: object
              properties:
                status:
                  $ref: '#/definitions/StatusObject'
            ErrorObject:
              type: array
              description: >-
                The errors member contains additional information about a failed
                request.
              items:
                type: object
                properties:
                  details:
                    type: string
                    description: >-
                      A human-readable, unstructured explanation specific to
                      this occurrence of the failure.
                  encryptedDetails:
                    type: string
                    description: >-
                      Base64-encoded, internal details about the error, in
                      addition to "details".
                  type:
                    type: number
                    format: int32
                    description: Internal error type of the Foundation API protocol.
                  attribute:
                    type: array
                    description: >-
                      For a validation error, a reference to the request
                      parameter that failed validation; otherwise, an empty
                      array.
                    items:
                      type: object
                      properties:
                        name:
                          type: string
                          description: Element of the path denoting the request parameter.
                        index:
                          type: number
                          format: int32
                          description: >-
                            If the attribute "name" designates an array, index
                            of the array element; otherwise the special value
                            -1.
                      x-property-sort:
                        - name
                        - index
                x-property-sort:
                  - detail
                  - encryptedDetails
                  - type
                  - attribute
            AttributesMember:
              type: array
              description: >-
                Limit the attributes returned in the response to the specified
                set.
              items:
                type: string
                maxLength: 100
                exclusiveMaximum: false
              maxItems: 50
              uniqueItems: true
            LanguageMember:
              type: string
              format: isoLanguage
              description: ISO 639-1 code of the language.
              maxLength: 2
              minLength: 2
              exclusiveMinimum: false
              exclusiveMaximum: false
            StatusObject:
              type: object
              properties:
                code:
                  type: number
                  format: int32
                  description: >-
                    The HTTP status code of the response, mirroring the code
                    from the Status-Line of the HTTP response message (see
                    [RFC2616] section 6.1).
              description: The status member contains the status code of the response.
              required:
                - code
            CursorBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the cursor-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of `total` is estimated.
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - total
                - isEstimatedTotal
                - next
                - previous
              x-property-sort:
                - total
                - isEstimatedTotal
                - next
                - previous
            CursorBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the cursor-based pagination strategy;
                a total element count is not supported.
              properties:
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - next
                - previous
              x-property-sort:
                - next
                - previous
            OffsetBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the offset-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of "total" is estimated.
              required:
                - total
                - isEstimatedTotal
              x-property-sort:
                - total
                - isEstimatedTotal
            OffsetBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the offset-based pagination strategy;
                a total element count is not supported.
              properties:
                hasNext:
                  type: boolean
                  description: >-
                    Flag indicating that a subsequent request with the same
                    parameters, except that the parameter `pagination.offset` is
                    incremented by `pagination.limit`, would yield additional
                    results.
              required:
                - hasNext
              x-property-sort:
                - hasNext
            PartialOutputObject:
              type: object
              properties:
                isPartial:
                  type: boolean
                  description: >-
                    Flag indicating that the response is a possibly incomplete
                    array or an object containing a possibly incomplete array,
                    due to hitting a processing time limit. If `true`, some
                    matching results might be missing from the array, or
                    elements for matching results might be incorrectly included
                    (for example, when priority sorting would have removed the
                    element). Depending on the use case, such a response may be
                    unsuitable.
              description: >-
                Object denoting that the endpoint response is possibly
                incomplete.
              required:
                - isPartial
              x-property-sort:
                - isPartial
          basePath: /wealth/v1
          schemes:
            - https
          securityDefinitions:
            Basic:
              type: nu
    overlays:
      - type: APIs.io Search
        url: overlays/etf-profile-and-prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/etf-profile-and-prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-etf-profile-and-prices-api
  - name: FactSet Investment Banking Office Refresh API
    description: Refresh FactSet models (e.g., Excel templates with =FDS codes).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/investment-banking-office-refresh-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Investment Banking Office Refresh API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          paths:
            /refresh/calculate:
              post:
                summary: Upload a spreadsheet file
                description: >-
                  Upload a spreadsheet file (in the Open Office XML format) for
                  FactSet to refresh.
                tags:
                  - Upload
                  - Spreadsheet
                  - File
                  - Refresh
                  - Calculate
            /refresh/{id}/status:
              get:
                summary: Get the status of the refresh job with the given resource ID
                description: Check the status of the given job by the resource ID
                tags:
                  - Get
                  - The
                  - Status
                  - Of
                  - Refresh
                  - Job
                  - With
                  - Given
                  - Resource
                  - Refresh
                  - Calculate
                  - Id
                  - Status
            /refresh/{id}:
              get:
                summary: Retrieve a calculated file by resource ID.
                description: >-
                  If the requested job is complete, the calculated file will be
                  returned.
                tags:
                  - Retrieve
                  - Calculated
                  - File
                  - By
                  - Resource
                  - D.
                  - Refresh
                  - Calculate
                  - Id
                  - Status
          tags:
            - name: nu
    overlays:
      - type: APIs.io Search
        url: overlays/investment-banking-office-refresh-openapi-original.yml
      - type: APIs.io Search
        url: overlays/investment-banking-office-refresh-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/investment-banking-office-refresh-openapi-api-evangelist-ratings.yml
    aid: factset:factset-investment-banking-office-refresh-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---