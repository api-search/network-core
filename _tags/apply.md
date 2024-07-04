---
name: Apply
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/apply.png
url: https://example.com/apis/apply.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Apply
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
  - name: clouddirectory
    description: >-
      <fullname>Amazon Cloud Directory</fullname> <p>Amazon Cloud Directory is a
      component of the AWS Directory Service that simplifies the development and
      management of cloud-scale web, mobile, and IoT applications. This guide
      describes the Cloud Directory operations that you can call
      programmatically and includes detailed information on data types and
      errors. For information about AWS Directory Services features, see <a
      href="https://aws.amazon.com/directoryservice/">AWS Directory Service</a>
      and the <a
      href="http://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html">AWS
      Directory Service Administration Guide</a>.</p>
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
            title: clouddirectory
          paths:
            /amazonclouddirectory/2017-01-11/object/facets:
              PUT:
                summary: AddFacetToObject
                description: >-
                  <p>Adds a new <a>Facet</a> to an object. An object can have
                  more than one facet applied on it.</p>
                tags:
                  - Add
                  - Facets
                  - To
                  - Objects
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
            /amazonclouddirectory/2017-01-11/schema/apply:
              PUT:
                summary: ApplySchema
                description: >-
                  <p>Copies the input published schema, at the specified
                  version, into the <a>Directory</a> with the same name and
                  version as that of the published schema.</p>
                tags:
                  - Apply
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
            /amazonclouddirectory/2017-01-11/object/attach:
              PUT:
                summary: AttachObject
                description: >-
                  <p>Attaches an existing object to another object. An object
                  can be accessed in two ways:</p> <ol> <li> <p>Using the
                  path</p> </li> <li> <p>Using <code>ObjectIdentifier</code>
                  </p> </li> </ol>
                tags:
                  - Attach
                  - Objects
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
            /amazonclouddirectory/2017-01-11/policy/attach:
              PUT:
                summary: AttachPolicy
                description: >-
                  <p>Attaches a policy object to a regular object. An object can
                  have a limited number of attached policies.</p>
                tags:
                  - Attach
                  - Policies
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
            /amazonclouddirectory/2017-01-11/index/attach:
              PUT:
                summary: AttachToIndex
                description: <p>Attaches the specified object to the specified index.</p>
                tags:
                  - Attach
                  - To
                  - Index
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
            /amazonclouddirectory/2017-01-11/typedlink/attach:
              PUT:
                summary: AttachTypedLink
                description: >-
                  <p>Attaches a typed link to a specified source and target
                  object. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Attach
                  - Typed
                  - Link
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
            /amazonclouddirectory/2017-01-11/batchread:
              POST:
                summary: BatchRead
                description: <p>Performs all the read operations in a batch. </p>
                tags:
                  - Batches
                  - Read
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
            /amazonclouddirectory/2017-01-11/batchwrite:
              PUT:
                summary: BatchWrite
                description: >-
                  <p>Performs all the write operations in a batch. Either all
                  the operations succeed or none.</p>
                tags:
                  - Batches
                  - Write
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
            /amazonclouddirectory/2017-01-11/directory/create:
              PUT:
                summary: CreateDirectory
                description: >-
                  <p>Creates a <a>Directory</a> by copying the published schema
                  into the directory. A directory cannot be created without a
                  schema.</p> <p>You can also quickly create a directory using a
                  managed schema, called the <code>QuickStartSchema</code>. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/schemas_managed.html">Managed
                  Schema</a> in the <i>Amazon Cloud Directory Developer
                  Guide</i>.</p>
                tags:
                  - Create
                  - Directory
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
            /amazonclouddirectory/2017-01-11/facet/create:
              PUT:
                summary: CreateFacet
                description: >-
                  <p>Creates a new <a>Facet</a> in a schema. Facet creation is
                  allowed only in development or applied schemas.</p>
                tags:
                  - Create
                  - Facets
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
            /amazonclouddirectory/2017-01-11/index:
              PUT:
                summary: CreateIndex
                description: >-
                  <p>Creates an index object. See <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/indexing_search.html">Indexing
                  and search</a> for more information.</p>
                tags:
                  - Create
                  - Index
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
            /amazonclouddirectory/2017-01-11/object:
              PUT:
                summary: CreateObject
                description: >-
                  <p>Creates an object in a <a>Directory</a>. Additionally
                  attaches the object to a parent, if a parent reference and
                  <code>LinkName</code> is specified. An object is simply a
                  collection of <a>Facet</a> attributes. You can also use this
                  API call to create a policy object, if the facet from which
                  you create the object is a policy facet. </p>
                tags:
                  - Create
                  - Objects
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
            /amazonclouddirectory/2017-01-11/schema/create:
              PUT:
                summary: CreateSchema
                description: >-
                  <p>Creates a new schema in a development state. A schema can
                  exist in three phases:</p> <ul> <li> <p> <i>Development:</i>
                  This is a mutable phase of the schema. All new schemas are in
                  the development phase. Once the schema is finalized, it can be
                  published.</p> </li> <li> <p> <i>Published:</i> Published
                  schemas are immutable and have a version associated with
                  them.</p> </li> <li> <p> <i>Applied:</i> Applied schemas are
                  mutable in a way that allows you to add new schema facets. You
                  can also add new, nonrequired attributes to existing schema
                  facets. You can apply only published schemas to directories.
                  </p> </li> </ul>
                tags:
                  - Create
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
            /amazonclouddirectory/2017-01-11/typedlink/facet/create:
              PUT:
                summary: CreateTypedLinkFacet
                description: >-
                  <p>Creates a <a>TypedLinkFacet</a>. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Create
                  - Typed
                  - Link
                  - Facets
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
            /amazonclouddirectory/2017-01-11/directory:
              PUT:
                summary: DeleteDirectory
                description: >-
                  <p>Deletes a directory. Only disabled directories can be
                  deleted. A deleted directory cannot be undone. Exercise
                  extreme caution when deleting directories.</p>
                tags:
                  - Delete
                  - Directory
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
            /amazonclouddirectory/2017-01-11/facet/delete:
              PUT:
                summary: DeleteFacet
                description: >-
                  <p>Deletes a given <a>Facet</a>. All attributes and
                  <a>Rule</a>s that are associated with the facet will be
                  deleted. Only development schema facets are allowed
                  deletion.</p>
                tags:
                  - Delete
                  - Facets
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
            /amazonclouddirectory/2017-01-11/object/delete:
              PUT:
                summary: DeleteObject
                description: >-
                  <p>Deletes an object and its associated attributes. Only
                  objects with no children and no parents can be deleted. The
                  maximum number of attributes that can be deleted during an
                  object deletion is 30. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/limits.html">Amazon
                  Cloud Directory Limits</a>.</p>
                tags:
                  - Delete
                  - Objects
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
            /amazonclouddirectory/2017-01-11/schema:
              PUT:
                summary: DeleteSchema
                description: >-
                  <p>Deletes a given schema. Schemas in a development and
                  published state can only be deleted. </p>
                tags:
                  - Delete
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
            /amazonclouddirectory/2017-01-11/typedlink/facet/delete:
              PUT:
                summary: DeleteTypedLinkFacet
                description: >-
                  <p>Deletes a <a>TypedLinkFacet</a>. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Delete
                  - Typed
                  - Link
                  - Facets
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
            /amazonclouddirectory/2017-01-11/index/detach:
              PUT:
                summary: DetachFromIndex
                description: <p>Detaches the specified object from the specified index.</p>
                tags:
                  - Detach
                  - From
                  - Index
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
            /amazonclouddirectory/2017-01-11/object/detach:
              PUT:
                summary: DetachObject
                description: >-
                  <p>Detaches a given object from the parent object. The object
                  that is to be detached from the parent is specified by the
                  link name.</p>
                tags:
                  - Detach
                  - Objects
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
            /amazonclouddirectory/2017-01-11/policy/detach:
              PUT:
                summary: DetachPolicy
                description: <p>Detaches a policy from an object.</p>
                tags:
                  - Detach
                  - Policies
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
            /amazonclouddirectory/2017-01-11/typedlink/detach:
              PUT:
                summary: DetachTypedLink
                description: >-
                  <p>Detaches a typed link from a specified source and target
                  object. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Detach
                  - Typed
                  - Link
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
            /amazonclouddirectory/2017-01-11/directory/disable:
              PUT:
                summary: DisableDirectory
                description: >-
                  <p>Disables the specified directory. Disabled directories
                  cannot be read or written to. Only enabled directories can be
                  disabled. Disabled directories may be reenabled.</p>
                tags:
                  - Disable
                  - Directory
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
            /amazonclouddirectory/2017-01-11/directory/enable:
              PUT:
                summary: EnableDirectory
                description: >-
                  <p>Enables the specified directory. Only disabled directories
                  can be enabled. Once enabled, the directory can then be read
                  and written to.</p>
                tags:
                  - Enable
                  - Directory
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
            /amazonclouddirectory/2017-01-11/schema/getappliedschema:
              POST:
                summary: GetAppliedSchemaVersion
                description: >-
                  <p>Returns current applied schema version ARN, including the
                  minor version in use.</p>
                tags:
                  - Get
                  - Applied
                  - Schemas
                  - Versions
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
            /amazonclouddirectory/2017-01-11/directory/get:
              POST:
                summary: GetDirectory
                description: <p>Retrieves metadata about a directory.</p>
                tags:
                  - Get
                  - Directory
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
            /amazonclouddirectory/2017-01-11/facet:
              PUT:
                summary: UpdateFacet
                description: >-
                  <p>Does the following:</p> <ol> <li> <p>Adds new
                  <code>Attributes</code>, <code>Rules</code>, or
                  <code>ObjectTypes</code>.</p> </li> <li> <p>Updates existing
                  <code>Attributes</code>, <code>Rules</code>, or
                  <code>ObjectTypes</code>.</p> </li> <li> <p>Deletes existing
                  <code>Attributes</code>, <code>Rules</code>, or
                  <code>ObjectTypes</code>.</p> </li> </ol>
                tags:
                  - Update
                  - Facets
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
            /amazonclouddirectory/2017-01-11/typedlink/attributes/get:
              POST:
                summary: GetLinkAttributes
                description: >-
                  <p>Retrieves attributes that are associated with a typed
                  link.</p>
                tags:
                  - Get
                  - Link
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
            /amazonclouddirectory/2017-01-11/object/attributes/get:
              POST:
                summary: GetObjectAttributes
                description: >-
                  <p>Retrieves attributes within a facet that are associated
                  with an object.</p>
                tags:
                  - Get
                  - Objects
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
            /amazonclouddirectory/2017-01-11/object/information:
              POST:
                summary: GetObjectInformation
                description: <p>Retrieves metadata about an object.</p>
                tags:
                  - Get
                  - Objects
                  - Information
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
            /amazonclouddirectory/2017-01-11/schema/json:
              PUT:
                summary: PutSchemaFromJson
                description: >-
                  <p>Allows a schema to be updated using JSON upload. Only
                  available for development schemas. See <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/schemas_jsonformat.html#schemas_json">JSON
                  Schema Format</a> for more information.</p>
                tags:
                  - Put
                  - Schemas
                  - From
                  - JSON
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
            /amazonclouddirectory/2017-01-11/typedlink/facet/get:
              POST:
                summary: GetTypedLinkFacetInformation
                description: >-
                  <p>Returns the identity attribute order for a specific
                  <a>TypedLinkFacet</a>. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Get
                  - Typed
                  - Link
                  - Facets
                  - Information
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
            /amazonclouddirectory/2017-01-11/schema/applied:
              POST:
                summary: ListAppliedSchemaArns
                description: >-
                  <p>Lists schema major versions applied to a directory. If
                  <code>SchemaArn</code> is provided, lists the minor
                  version.</p>
                tags:
                  - Lists
                  - Applied
                  - Schemas
                  - ARN
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
            /amazonclouddirectory/2017-01-11/object/indices:
              POST:
                summary: ListAttachedIndices
                description: <p>Lists indices attached to the specified object.</p>
                tags:
                  - Lists
                  - Attached
                  - Indices
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
            /amazonclouddirectory/2017-01-11/schema/development:
              POST:
                summary: ListDevelopmentSchemaArns
                description: >-
                  <p>Retrieves each Amazon Resource Name (ARN) of schemas in the
                  development state.</p>
                tags:
                  - Lists
                  - Development
                  - Schemas
                  - ARN
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
            /amazonclouddirectory/2017-01-11/directory/list:
              POST:
                summary: ListDirectories
                description: <p>Lists directories created within an account.</p>
                tags:
                  - Lists
                  - Directories
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
            /amazonclouddirectory/2017-01-11/facet/attributes:
              POST:
                summary: ListFacetAttributes
                description: <p>Retrieves attributes attached to the facet.</p>
                tags:
                  - Lists
                  - Facets
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
            /amazonclouddirectory/2017-01-11/facet/list:
              POST:
                summary: ListFacetNames
                description: <p>Retrieves the names of facets that exist in a schema.</p>
                tags:
                  - Lists
                  - Facets
                  - Names
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
            /amazonclouddirectory/2017-01-11/typedlink/incoming:
              POST:
                summary: ListIncomingTypedLinks
                description: >-
                  <p>Returns a paginated list of all the incoming
                  <a>TypedLinkSpecifier</a> information for an object. It also
                  supports filtering by typed link facet and identity
                  attributes. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Lists
                  - Incoming
                  - Typed
                  - Links
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
            /amazonclouddirectory/2017-01-11/index/targets:
              POST:
                summary: ListIndex
                description: <p>Lists objects attached to the specified index.</p>
                tags:
                  - Lists
                  - Index
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
            /amazonclouddirectory/2017-01-11/schema/managed:
              POST:
                summary: ListManagedSchemaArns
                description: >-
                  <p>Lists the major version families of each managed schema. If
                  a major version ARN is provided as SchemaArn, the minor
                  version revisions in that family are listed instead.</p>
                tags:
                  - Lists
                  - Managed
                  - Schemas
                  - ARN
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
            /amazonclouddirectory/2017-01-11/object/attributes:
              POST:
                summary: ListObjectAttributes
                description: >-
                  <p>Lists all attributes that are associated with an object.
                  </p>
                tags:
                  - Lists
                  - Objects
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
            /amazonclouddirectory/2017-01-11/object/children:
              POST:
                summary: ListObjectChildren
                description: >-
                  <p>Returns a paginated list of child objects that are
                  associated with a given object.</p>
                tags:
                  - Lists
                  - Objects
                  - Children
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
            /amazonclouddirectory/2017-01-11/object/parentpaths:
              POST:
                summary: ListObjectParentPaths
                description: >-
                  <p>Retrieves all available parent paths for any object type
                  such as node, leaf node, policy node, and index node objects.
                  For more information about objects, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/key_concepts_directorystructure.html">Directory
                  Structure</a>.</p> <p>Use this API to evaluate all parents for
                  an object. The call returns all objects from the root of the
                  directory up to the requested object. The API returns the
                  number of paths based on user-defined <code>MaxResults</code>,
                  in case there are multiple paths to the parent. The order of
                  the paths and nodes returned is consistent among multiple API
                  calls unless the objects are deleted or moved. Paths not
                  leading to the directory root are ignored from the target
                  object.</p>
                tags:
                  - Lists
                  - Objects
                  - Parents
                  - Paths
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
            /amazonclouddirectory/2017-01-11/object/parent:
              POST:
                summary: ListObjectParents
                description: >-
                  <p>Lists parent objects that are associated with a given
                  object in pagination fashion.</p>
                tags:
                  - Lists
                  - Objects
                  - Parents
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
            /amazonclouddirectory/2017-01-11/object/policy:
              POST:
                summary: ListObjectPolicies
                description: >-
                  <p>Returns policies attached to an object in pagination
                  fashion.</p>
                tags:
                  - Lists
                  - Objects
                  - Policies
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
            /amazonclouddirectory/2017-01-11/typedlink/outgoing:
              POST:
                summary: ListOutgoingTypedLinks
                description: >-
                  <p>Returns a paginated list of all the outgoing
                  <a>TypedLinkSpecifier</a> information for an object. It also
                  supports filtering by typed link facet and identity
                  attributes. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Lists
                  - Outgoing
                  - Typed
                  - Links
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
            /amazonclouddirectory/2017-01-11/policy/attachment:
              POST:
                summary: ListPolicyAttachments
                description: >-
                  <p>Returns all of the <code>ObjectIdentifiers</code> to which
                  a given policy is attached.</p>
                tags:
                  - Lists
                  - Policies
                  - Attachments
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
            /amazonclouddirectory/2017-01-11/schema/published:
              POST:
                summary: ListPublishedSchemaArns
                description: >-
                  <p>Lists the major version families of each published schema.
                  If a major version ARN is provided as <code>SchemaArn</code>,
                  the minor version revisions in that family are listed
                  instead.</p>
                tags:
                  - Lists
                  - Published
                  - Schemas
                  - ARN
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
            /amazonclouddirectory/2017-01-11/tags:
              POST:
                summary: ListTagsForResource
                description: >-
                  <p>Returns tags for a resource. Tagging is currently supported
                  only for directories with a limit of 50 tags per directory.
                  All 50 tags are returned for a given directory with this API
                  call.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
            /amazonclouddirectory/2017-01-11/typedlink/facet/attributes:
              POST:
                summary: ListTypedLinkFacetAttributes
                description: >-
                  <p>Returns a paginated list of all attribute definitions for a
                  particular <a>TypedLinkFacet</a>. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Lists
                  - Typed
                  - Link
                  - Facets
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
            /amazonclouddirectory/2017-01-11/typedlink/facet/list:
              POST:
                summary: ListTypedLinkFacetNames
                description: >-
                  <p>Returns a paginated list of <code>TypedLink</code> facet
                  names for a particular schema. For more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Lists
                  - Typed
                  - Link
                  - Facets
                  - Names
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
            /amazonclouddirectory/2017-01-11/policy/lookup:
              POST:
                summary: LookupPolicy
                description: >-
                  <p>Lists all policies from the root of the <a>Directory</a> to
                  the object specified. If there are no policies present, an
                  empty list is returned. If policies are present, and if some
                  objects don't have the policies attached, it returns the
                  <code>ObjectIdentifier</code> for such objects. If policies
                  are present, it returns <code>ObjectIdentifier</code>,
                  <code>policyId</code>, and <code>policyType</code>. Paths that
                  don't lead to the root from the target object are ignored. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/key_concepts_directory.html#key_concepts_policies">Policies</a>.</p>
                tags:
                  - Lookups
                  - Policies
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
            /amazonclouddirectory/2017-01-11/schema/publish:
              PUT:
                summary: PublishSchema
                description: >-
                  <p>Publishes a development schema with a major version and a
                  recommended minor version.</p>
                tags:
                  - Publish
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
            /amazonclouddirectory/2017-01-11/object/facets/delete:
              PUT:
                summary: RemoveFacetFromObject
                description: <p>Removes the specified facet from the specified object.</p>
                tags:
                  - Removes
                  - Facets
                  - From
                  - Objects
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
            /amazonclouddirectory/2017-01-11/tags/add:
              PUT:
                summary: TagResource
                description: <p>An API operation for adding tags to a resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
            /amazonclouddirectory/2017-01-11/tags/remove:
              PUT:
                summary: UntagResource
                description: <p>An API operation for removing tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
            /amazonclouddirectory/2017-01-11/typedlink/attributes/update:
              POST:
                summary: UpdateLinkAttributes
                description: >-
                  <p>Updates a given typed link’s attributes. Attributes to be
                  updated must not contribute to the typed link’s identity, as
                  defined by its <code>IdentityAttributeOrder</code>.</p>
                tags:
                  - Update
                  - Link
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
                  - Update
            /amazonclouddirectory/2017-01-11/object/update:
              PUT:
                summary: UpdateObjectAttributes
                description: <p>Updates a given object's attributes.</p>
                tags:
                  - Update
                  - Objects
                  - Attributes
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
                  - Update
            /amazonclouddirectory/2017-01-11/schema/update:
              PUT:
                summary: UpdateSchema
                description: >-
                  <p>Updates the schema name with a new name. Only development
                  schema names can be updated.</p>
                tags:
                  - Update
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
                  - Update
            /amazonclouddirectory/2017-01-11/typedlink/facet:
              PUT:
                summary: UpdateTypedLinkFacet
                description: >-
                  <p>Updates a <a>TypedLinkFacet</a>. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/clouddirectory/latest/developerguide/directory_objects_links.html#directory_objects_links_typedlink">Typed
                  Links</a>.</p>
                tags:
                  - Update
                  - Typed
                  - Link
                  - Facets
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
                  - Update
            /amazonclouddirectory/2017-01-11/schema/upgradeapplied:
              PUT:
                summary: UpgradeAppliedSchema
                description: >-
                  <p>Upgrades a single directory in-place using the
                  <code>PublishedSchemaArn</code> with schema updates found in
                  <code>MinorVersion</code>. Backwards-compatible minor version
                  upgrades are instantaneously available for readers on all
                  objects in the directory. Note: This is a synchronous API call
                  and upgrades only one schema on a given directory per call. To
                  upgrade multiple directories from one schema, you would need
                  to call this API on each directory.</p>
                tags:
                  - Upgrade
                  - Applied
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
                  - Update
                  - Upgrade Applied
            /amazonclouddirectory/2017-01-11/schema/upgradepublished:
              PUT:
                summary: UpgradePublishedSchema
                description: >-
                  <p>Upgrades a published schema under a new minor version
                  revision using the current contents of
                  <code>DevelopmentSchemaArn</
                tags:
                  - Upgrade
                  - Published
                  - Schemas
                  - Amazon Cloud Directory
                  - '2017'
                  - '01'
                  - '11'
                  - Objects
                  - Facets
                  - Schemas
                  - Apply
                  - Attach
                  - Policies
                  - Index
                  - Typed Links
                  - Batches
                  - Batches
                  - Directory
                  - Create
                  - Facets
                  - Delete
                  - Detach
                  - Disable
                  - Enable
                  - Applied Schema
                  - Get
                  - Attributes
                  - Information
                  - JSON
                  - Applied
                  - Indices
                  - Development
                  - Lists
                  - Incoming
                  - Targets
                  - Managed
                  - Children
                  - Parent Paths
                  - Parents
                  - Outgoing
                  - Attachment
                  - Published
                  - Tags
                  - Lookups
                  - Publish
                  - Add
                  - Removes
                  - Update
                  - Upgrade Applied
                  - Upgrade Publish
    overlays:
      - type: APIs.io Search
        url: overlays/clouddirectory-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/clouddirectory-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:clouddirectory
  - name: rum
    description: >-
      <p>With Amazon CloudWatch RUM, you can perform real-user monitoring to
      collect client-side data about your web application performance from
      actual user sessions in real time. The data collected includes page load
      times, client-side errors, and user behavior. When you view this data, you
      can see it all aggregated together and also see breakdowns by the browsers
      and devices that your customers use.</p> <p>You can use the collected data
      to quickly identify and debug client-side performance issues. CloudWatch
      RUM helps you visualize anomalies in your application performance and find
      relevant debugging data such as error messages, stack traces, and user
      sessions. You can also use RUM to understand the range of end-user impact
      including the number of users, geolocations, and browsers used.</p>
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
            title: rum
          paths:
            /rummetrics/{AppMonitorName}/metrics:
              PATCH:
                summary: UpdateRumMetricDefinition
                description: >-
                  <p>Modifies one existing metric definition for CloudWatch RUM
                  extended metrics. For more information about extended metrics,
                  see <a
                  href="https://docs.aws.amazon.com/cloudwatchrum/latest/APIReference/API_BatchCreateRumMetricsDefinitions.html">BatchCreateRumMetricsDefinitions</a>.</p>
                tags:
                  - Update
                  - Rum
                  - Metrics
                  - Definitions
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
            /appmonitor:
              POST:
                summary: CreateAppMonitor
                description: >-
                  <p>Creates a Amazon CloudWatch RUM app monitor, which collects
                  telemetry data from your application and sends that data to
                  RUM. The data includes performance and reliability information
                  such as page load time, client-side errors, and user
                  behavior.</p> <p>You use this operation only to create a new
                  app monitor. To update an existing app monitor, use <a
                  href="https://docs.aws.amazon.com/cloudwatchrum/latest/APIReference/API_UpdateAppMonitor.html">UpdateAppMonitor</a>
                  instead.</p> <p>After you create an app monitor, sign in to
                  the CloudWatch RUM console to get the JavaScript code snippet
                  to add to your web application. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-find-code-snippet.html">How
                  do I find a code snippet that I've already generated?</a> </p>
                tags:
                  - Create
                  - Applications
                  - Monitors
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
            /appmonitor/{Name}:
              PATCH:
                summary: UpdateAppMonitor
                description: >-
                  <p>Updates the configuration of an existing app monitor. When
                  you use this operation, only the parts of the app monitor
                  configuration that you specify in this operation are changed.
                  For any parameters that you omit, the existing values are
                  kept.</p> <p>You can't use this operation to change the tags
                  of an existing app monitor. To change the tags of an existing
                  app monitor, use <a
                  href="https://docs.aws.amazon.com/cloudwatchrum/latest/APIReference/API_TagResource.html">TagResource</a>.</p>
                  <p>To create a new app monitor, use <a
                  href="https://docs.aws.amazon.com/cloudwatchrum/latest/APIReference/API_CreateAppMonitor.html">CreateAppMonitor</a>.</p>
                  <p>After you update an app monitor, sign in to the CloudWatch
                  RUM console to get the updated JavaScript code snippet to add
                  to your web application. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-find-code-snippet.html">How
                  do I find a code snippet that I've already generated?</a> </p>
                tags:
                  - Update
                  - Applications
                  - Monitors
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
            /rummetrics/{AppMonitorName}/metricsdestination:
              POST:
                summary: PutRumMetricsDestination
                description: >-
                  <p>Creates or updates a destination to receive extended
                  metrics from CloudWatch RUM. You can send extended metrics to
                  CloudWatch or to a CloudWatch Evidently experiment.</p> <p>For
                  more information about extended metrics, see <a
                  href="https://docs.aws.amazon.com/cloudwatchrum/latest/APIReference/API_BatchCreateRumMetricDefinitions.html">BatchCreateRumMetricDefinitions</a>.</p>
                tags:
                  - Put
                  - Rum
                  - Metrics
                  - Destinations
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
                  - Metric Destination
            /appmonitor/{Name}/data:
              POST:
                summary: GetAppMonitorData
                description: >-
                  <p>Retrieves the raw performance events that RUM has collected
                  from your web application, so that you can do your own
                  processing or analysis of this data.</p>
                tags:
                  - Get
                  - Applications
                  - Monitors
                  - Data
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
                  - Metric Destination
                  - Data
            /appmonitors:
              POST:
                summary: ListAppMonitors
                description: >-
                  <p>Returns a list of the Amazon CloudWatch RUM app monitors in
                  the account.</p>
                tags:
                  - Lists
                  - Applications
                  - Monitors
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
                  - Metric Destination
                  - Data
                  - Application Monitors
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
                  - Metric Destination
                  - Data
                  - Application Monitors
                  - Resources
                  - ARN
            /appmonitors/{Id}/:
              POST:
                summary: PutRumEvents
                description: >-
                  <p>Sends telemetry events about your application performance
                  and user behavior to CloudWatch RUM. The code snippet that RUM
                  generates for you to add to your application includes
                  <code>PutRumEvents</code> operations to send this data to
                  RUM.</p> <p>Each <code>PutRumEvents</code> operation can send
                  a batch of events from one user se
                tags:
                  - Put
                  - Rum
                  - Events
                  - Applications
                  - Monitors
                  - Names
                  - Metrics
                  - Apply
                  - Metric Destination
                  - Data
                  - Application Monitors
                  - Resources
                  - ARN
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/rum-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rum-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rum
  - aid: box:box-files-api
    name: Box Files API
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
            title: Box Files API
          paths:
            /files/{file_id}:
              get:
                summary: Get file information
                tags:
                  - Get
                  - File
                  - Information
                  - Files
                  - File_id
                description: Retrieves the details about a file.
              post:
                summary: Restore file
                tags:
                  - Restore
                  - File
                  - Files
                  - File_id
                description: >-
                  Restores a file that has been moved to the trash.


                  An optional new parent ID can be provided to restore the file
                  to in case the

                  original folder has been deleted.
              put:
                summary: Update file
                tags:
                  - Update
                  - File
                  - Files
                  - File_id
                description: |-
                  Updates a file. This can be used to rename or move a file,
                  create a shared link, or lock a file.
              delete:
                summary: Delete file
                tags:
                  - Delete
                  - File
                  - Files
                  - File_id
                description: |-
                  Deletes a file, either permanently or by moving it to
                  the trash.

                  The the enterprise settings determine whether the item will
                  be permanently deleted from Box or moved to the trash.
            /files/{file_id}/content:
              get:
                summary: Download file
                tags:
                  - Download
                  - File
                  - Files
                  - File_id
                  - Content
                description: Returns the contents of a file in binary format.
              post:
                tags:
                  - Upload
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                summary: Upload file version
                description: |-
                  Update a file's content. For file sizes over 50MB we recommend
                  using the Chunk Upload APIs.

                  # Request body order

                  The `attributes` part of the body must come **before** the
                  `file` part. Requests that do not follow this format when
                  uploading the file will receive a HTTP `400` error with a
                  `metadata_after_file_contents` error code.
            /files/content:
              options:
                summary: Preflight check before upload
                tags:
                  - Preflight
                  - Check
                  - Before
                  - Upload
                  - Files
                  - File_id
                  - Content
                description: |-
                  Performs a check to verify that a file will be accepted by Box
                  before you upload the entire file.
              post:
                tags:
                  - Upload
                  - File
                  - Files
                  - File_id
                  - Content
                summary: Upload file
                description: >-
                  Uploads a small file to Box. For file sizes over 50MB we
                  recommend

                  using the Chunk Upload APIs.


                  # Request body order


                  The `attributes` part of the body must come **before** the

                  `file` part. Requests that do not follow this format when

                  uploading the file will receive a HTTP `400` error with a

                  `metadata_after_file_contents` error code.
            /files/upload_sessions:
              post:
                summary: Create upload session
                tags:
                  - Create
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                description: Creates an upload session for a new file.
            /files/{file_id}/upload_sessions:
              post:
                summary: Create upload session for existing file
                tags:
                  - Create
                  - Upload
                  - Session
                  - For
                  - Existing
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                description: Creates an upload session for an existing file.
            /files/upload_sessions/{upload_session_id}:
              get:
                summary: Get upload session
                tags:
                  - Get
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: Return information about an upload session.
              put:
                summary: Upload part of file
                tags:
                  - Upload
                  - Part
                  - Of
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: Updates a chunk of an upload session for a file.
              delete:
                summary: Remove upload session
                tags:
                  - Remove
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: |-
                  Abort an upload session and discard all data uploaded.

                  This cannot be reversed.
            /files/upload_sessions/{upload_session_id}/parts:
              get:
                summary: List parts
                tags:
                  - List
                  - Parts
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                description: |-
                  Return a list of the chunks uploaded to the upload
                  session so far.
            /files/upload_sessions/{upload_session_id}/commit:
              post:
                summary: Commit upload session
                tags:
                  - Commit
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                description: |-
                  Close an upload session and create a file from the
                  uploaded chunks.
            /files/{file_id}/copy:
              post:
                summary: Copy file
                description: Creates a copy of a file.
                tags:
                  - Copy
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
            /files/{file_id}/thumbnail.{extension}:
              get:
                summary: Get file thumbnail
                description: >-
                  Retrieves a thumbnail, or smaller image representation, of a
                  file.


                  Sizes of `32x32`,`64x64`, `128x128`, and `256x256` can be
                  returned in

                  the `.png` format and sizes of `32x32`, `160x160`, and
                  `320x320`

                  can be returned in the `.jpg` format.


                  Thumbnails can be generated for the image and video file
                  formats listed

                  [found on our community site][1].


                  [1]:
                  https://community.box.com/t5/Migrating-and-Previewing-Content/File-Types-and-Fonts-Supported-in-Box-Content-Preview/ta-p/327
                tags:
                  - Get
                  - File
                  - Thumbnail
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
            /files/{file_id}/collaborations:
              get:
                summary: List file collaborations
                description: |-
                  Retrieves a list of pending and active collaborations for a
                  file. This returns all the users that have access to the file
                  or have been invited to the file.
                tags:
                  - List
                  - File
                  - Collaborations
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
            /files/{file_id}/comments:
              get:
                summary: List file comments
                description: Retrieves a list of comments for a file.
                tags:
                  - List
                  - File
                  - Comments
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
            /files/{file_id}/tasks:
              get:
                summary: List tasks on file
                description: |-
                  Retrieves a list of all the tasks for a file. This
                  endpoint does not support pagination.
                tags:
                  - List
                  - Tasks
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
            /files/{file_id}/trash:
              get:
                summary: Get trashed file
                tags:
                  - Get
                  - Trashed
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                description: >-
                  Retrieves a file that has been moved to the trash.


                  Please note that only if the file itself has been moved to the

                  trash can it be retrieved with this API call. If instead one
                  of

                  its parent folders was moved to the trash, only that folder

                  can be inspected using the

                  [`GET /folders/:id/trash`](e://get_folders_id_trash) API.


                  To list all items that have been moved to the trash, please

                  use the [`GET
                  /folders/trash/items`](e://get-folders-trash-items/)

                  API.
              delete:
                summary: Permanently remove file
                tags:
                  - Permanently
                  - Remove
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                description: |-
                  Permanently deletes a file that is in the trash.
                  This action cannot be undone.
            /files/{file_id}/versions:
              get:
                summary: List all file versions
                tags:
                  - List
                  - All
                  - File
                  - Versions
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                description: >-
                  Retrieve a list of the past versions for a file.


                  Versions are only tracked by Box users with premium accounts.
                  To fetch the ID

                  of the current version of a file, use the `GET /file/:id` API.
            /files/{file_id}/versions/{file_version_id}:
              get:
                summary: Get file version
                tags:
                  - Get
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Retrieve a specific version of a file.

                  Versions are only tracked for Box users with premium accounts.
              delete:
                summary: Remove file version
                tags:
                  - Remove
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Move a file version to the trash.

                  Versions are only tracked for Box users with premium accounts.
              put:
                summary: Restore file version
                tags:
                  - Restore
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Restores a specific version of a file after it was deleted.
                  Don't use this endpoint to restore Box Notes,
                  as it works with file formats such as PDF, DOC,
                  PPTX or similar.
            /files/{file_id}/versions/current:
              post:
                summary: Promote file version
                tags:
                  - Promote
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                description: >-
                  Promote a specific version of a file.


                  If previous versions exist, this method can be used to

                  promote one of the older versions to the top of the version
                  history.


                  This creates a new copy of the old version and puts it at the

                  top of the versions history. The file will have the exact same
                  contents

                  as the older version, with the the same hash digest, `etag`,
                  and

                  name as the original.


                  Other properties such as comments do not get updated to their

                  former values.


                  Don't use this endpoint to restore Box Notes,

                  as it works with file formats such as PDF, DOC,

                  PPTX or similar.
            /files/{file_id}/metadata:
              get:
                summary: List metadata instances on file
                tags:
                  - List
                  - Metadata
                  - Instances
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                description: Retrieves all metadata for a given file.
            /files/{file_id}/metadata/enterprise/securityClassification-6VMVochwUWo:
              get:
                summary: Get classification on file
                tags:
                  - Get
                  - Classification
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Retrieves the classification metadata instance that

                  has been applied to a file.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              post:
                summary: Add classification to file
                tags:
                  - Add
                  - Classification
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Adds a classification to a file by specifying the label of the

                  classification to add.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              put:
                summary: Update classification on file
                tags:
                  - Update
                  - Classification
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Updates a classification on a file.


                  The classification can only be updated if a classification has
                  already been

                  applied to the file before. When editing classifications, only
                  values are

                  defined for the enterprise will be accepted.
              delete:
                summary: Remove classification from file
                tags:
                  - Remove
                  - Classification
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Removes any classifications from a file.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
            /files/{file_id}/metadata/{scope}/{template_key}:
              get:
                summary: Get metadata instance on file
                tags:
                  - Get
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the instance of a metadata template that has been
                  applied to a

                  file.
              post:
                summary: Create metadata instance on file
                tags:
                  - Create
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Applies an instance of a metadata template to a file.


                  In most cases only values that are present in the metadata
                  template

                  will be accepted, except for the `global.properties` template
                  which accepts

                  any key-value pair.
              put:
                summary: Update metadata instance on file
                tags:
                  - Update
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Updates a piece of metadata on a file.


                  The metadata instance can only be updated if the template has
                  already been

                  applied to the file before. When editing metadata, only values
                  that match

                  the metadata template schema will be accepted.


                  The update is applied atomically. If any errors occur during
                  the

                  application of the operations, the metadata instance will not
                  be changed.
              delete:
                summary: Remove metadata instance from file
                tags:
                  - Remove
                  - Metadata
                  - Instance
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: Deletes a piece of file metadata.
            /files/{file_id}/metadata/global/boxSkillsCards:
              get:
                summary: List Box Skill cards on file
                tags:
                  - List
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: >-
                  List the Box Skills metadata cards that are attached to a
                  file.
              post:
                summary: Create Box Skill cards on file
                tags:
                  - Create
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Applies one or more Box Skills metadata cards to a file.
              put:
                summary: Update Box Skill cards on file
                tags:
                  - Update
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Updates one or more Box Skills metadata cards to a file.
              delete:
                summary: Remove Box Skill cards from file
                tags:
                  - Remove
                  - Box
                  - Skill
                  - Cards
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Removes any Box Skills cards metadata from a file.
            /files/{file_id}/watermark:
              get:
                summary: Get watermark on file
                tags:
                  - Get
                  - Watermark
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Retrieve the watermark for a file.
              put:
                summary: Apply watermark to file
                tags:
                  - Apply
                  - Watermark
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Applies or update a watermark on a file.
              delete:
                summary: Remove watermark from file
                tags:
                  - Remove
                  - Watermark
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Removes the watermark from a file.
            /files/{file_id}#get_shared_link:
              get:
                summary: Get shared link for file
                tags:
                  - Get
                  - Shared
                  - Link
                  - For
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                description: Gets the information for a shared link on a file.
            /files/{file_id}#add_shared_link:
              put:
                summary: Add shared link to file
                tags:
                  - Add
                  - Shared
                  - Link
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                description: Adds a shared link to a file.
            /files/{file_id}#update_shared_link:
              put:
                summary: Update shared link on file
                tags:
                  - Update
                  - Shared
                  - Link
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                description: Updates a shared link on a file.
            /files/{file_id}#remove_shared_link:
              put:
                summary: Remove shared link from file
                tags:
                  - Remove
                  - Shared
                  - Link
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                description: Removes a shared link from a file.
            /retention_policy_assignments/{retention_policy_assignment_id}/files_under_retention:
              get:
                summary: Get files under retention
                tags:
                  - Get
                  - Files
                  - Under
                  - Retention
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                description: >-
                  Returns a list of files under retention for a retention policy
                  assignment.
            /legal_hold_policy_assignments/{legal_hold_policy_assignment_id}/files_on_hold:
              get:
                summary: List current file versions for legal hold policy assignment
                tags:
                  - List
                  - Current
                  - File
                  - Versions
                  - For
                  - Legal
                  - Hold
                  - Policy
                  - Assignment
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                  - Legal_hold_policy_assignments
                  - Legal_hold_policy_assignment_id
                  - Files_on_hold
                description: >-
                  Get a list of current file versions for a legal hold

                  assignment.


                  In some cases you may want to get previous file versions
                  instead. In these

                  cases, use the `GET 
                  /legal_hold_policy_assignments/:id/file_versions_on_hold`

                  API instead to return any previous versions of a file for this
                  legal hold

                  policy assignment.


                  Due to ongoing re-architecture efforts this API might not
                  return all file

                  versions held for this policy ID. Instead, this API will only
                  return the

                  latest file version held in the newly developed architecture.
                  The `GET

                  /file_version_legal_holds` API can be used to fetch current
                  and past versions

                  of files held within the legacy architecture.


                  The `GET /legal_hold_policy_assignments?policy_id={id}` API
                  can be used to

                  find a list of policy assignments for a give
    overlays:
      - type: APIs.io Search
        url: overlays/files-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/files-openapi-api-evangelist-ratings.yml
  - aid: box:box-folders-api
    name: Box Folders API
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
            title: Box Folders API
          paths:
            /folders/{folder_id}:
              get:
                summary: Get folder information
                tags:
                  - Get
                  - Folder
                  - Information
                  - Folders
                  - Folder_id
                description: >-
                  Retrieves details for a folder, including the first 100
                  entries

                  in the folder.


                  Passing `sort`, `direction`, `offset`, and `limit`

                  parameters in query allows you to manage the

                  list of returned

                  [folder items](r://folder--full#param-item-collection).


                  To fetch more items within the folder, use the

                  [Get items in a folder](e://get-folders-id-items) endpoint.
              post:
                summary: Restore folder
                tags:
                  - Restore
                  - Folder
                  - Folders
                  - Folder_id
                description: >-
                  Restores a folder that has been moved to the trash.


                  An optional new parent ID can be provided to restore the
                  folder to in case the

                  original folder has been deleted.


                  # Folder locking


                  During this operation, part of the file tree will be locked,
                  mainly

                  the source folder and all of its descendants, as well as the
                  destination

                  folder.


                  For the duration of the operation, no other move, copy,
                  delete, or restore

                  operation can performed on any of the locked folders.
              put:
                summary: Update folder
                description: |-
                  Updates a folder. This can be also be used to move the folder,
                  create shared links, update collaborations, and more.
                tags:
                  - Update
                  - Folder
                  - Folders
                  - Folder_id
              delete:
                summary: Delete folder
                description: |-
                  Deletes a folder, either permanently or by moving it to
                  the trash.
                tags:
                  - Delete
                  - Folder
                  - Folders
                  - Folder_id
            /folders/{folder_id}/items:
              get:
                summary: List items in folder
                tags:
                  - List
                  - Items
                  - In
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                description: >-
                  Retrieves a page of items in a folder. These items can be
                  files,

                  folders, and web links.


                  To request more information about the folder itself, like its
                  size,

                  use the [Get a folder](#get-folders-id) endpoint instead.
            /folders:
              post:
                summary: Create folder
                tags:
                  - Create
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                description: Creates a new empty folder within the specified parent folder.
            /folders/{folder_id}/copy:
              post:
                summary: Copy folder
                description: |-
                  Creates a copy of a folder within a destination folder.

                  The original folder will not be changed.
                tags:
                  - Copy
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
            /folders/{folder_id}/collaborations:
              get:
                summary: List folder collaborations
                description: >-
                  Retrieves a list of pending and active collaborations for a

                  folder. This returns all the users that have access to the
                  folder

                  or have been invited to the folder.
                tags:
                  - List
                  - Folder
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
            /folders/{folder_id}/trash:
              get:
                summary: Get trashed folder
                tags:
                  - Get
                  - Trashed
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                description: >-
                  Retrieves a folder that has been moved to the trash.


                  Please note that only if the folder itself has been moved to
                  the

                  trash can it be retrieved with this API call. If instead one
                  of

                  its parent folders was moved to the trash, only that folder

                  can be inspected using the

                  [`GET /folders/:id/trash`](e://get_folders_id_trash) API.


                  To list all items that have been moved to the trash, please

                  use the [`GET
                  /folders/trash/items`](e://get-folders-trash-items/)

                  API.
              delete:
                summary: Permanently remove folder
                tags:
                  - Permanently
                  - Remove
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                description: |-
                  Permanently deletes a folder that is in the trash.
                  This action cannot be undone.
            /folders/{folder_id}/metadata:
              get:
                summary: List metadata instances on folder
                tags:
                  - List
                  - Metadata
                  - Instances
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                description: >-
                  Retrieves all metadata for a given folder. This can not be
                  used on the root

                  folder with ID `0`.
            /folders/{folder_id}/metadata/enterprise/securityClassification-6VMVochwUWo:
              get:
                summary: Get classification on folder
                tags:
                  - Get
                  - Classification
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Retrieves the classification metadata instance that

                  has been applied to a folder.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/folders/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              post:
                summary: Add classification to folder
                tags:
                  - Add
                  - Classification
                  - To
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Adds a classification to a folder by specifying the label of
                  the

                  classification to add.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/folders/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              put:
                summary: Update classification on folder
                tags:
                  - Update
                  - Classification
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Updates a classification on a folder.


                  The classification can only be updated if a classification has
                  already been

                  applied to the folder before. When editing classifications,
                  only values are

                  defined for the enterprise will be accepted.
              delete:
                summary: Remove classification from folder
                tags:
                  - Remove
                  - Classification
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Removes any classifications from a folder.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/folders/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
            /folders/{folder_id}/metadata/{scope}/{template_key}:
              get:
                summary: Get metadata instance on folder
                tags:
                  - Get
                  - Metadata
                  - Instance
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the instance of a metadata template that has been
                  applied to a

                  folder. This can not be used on the root folder with ID `0`.
              post:
                summary: Create metadata instance on folder
                tags:
                  - Create
                  - Metadata
                  - Instance
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Applies an instance of a metadata template to a folder.


                  In most cases only values that are present in the metadata
                  template

                  will be accepted, except for the `global.properties` template
                  which accepts

                  any key-value pair.


                  To display the metadata template in the Box web app the
                  enterprise needs to be

                  configured to enable **Cascading Folder Level Metadata** for
                  the user in the

                  admin console.
              put:
                summary: Update metadata instance on folder
                tags:
                  - Update
                  - Metadata
                  - Instance
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Updates a piece of metadata on a folder.


                  The metadata instance can only be updated if the template has
                  already been

                  applied to the folder before. When editing metadata, only
                  values that match

                  the metadata template schema will be accepted.


                  The update is applied atomically. If any errors occur during
                  the

                  application of the operations, the metadata instance will not
                  be changed.
              delete:
                summary: Remove metadata instance from folder
                tags:
                  - Remove
                  - Metadata
                  - Instance
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: Deletes a piece of folder metadata.
            /folders/trash/items:
              get:
                summary: List trashed items
                tags:
                  - List
                  - Trashed
                  - Items
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the files and folders that have been moved

                  to the trash.


                  Any attribute in the full files or folders objects can be
                  passed

                  in with the `fields` parameter to retrieve those specific

                  attributes that are not returned by default.


                  This endpoint defaults to use offset-based pagination, yet
                  also supports

                  marker-based pagination using the `marker` parameter.
            /folders/{folder_id}/watermark:
              get:
                summary: Get watermark for folder
                tags:
                  - Get
                  - Watermark
                  - For
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                description: Retrieve the watermark for a folder.
              put:
                summary: Apply watermark to folder
                tags:
                  - Apply
                  - Watermark
                  - To
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                description: Applies or update a watermark on a folder.
              delete:
                summary: Remove watermark from folder
                tags:
                  - Remove
                  - Watermark
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                description: Removes the watermark from a folder.
            /folders/{folder_id}#get_shared_link:
              get:
                summary: Get shared link for folder
                tags:
                  - Get
                  - Shared
                  - Link
                  - For
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                description: Gets the information for a shared link on a folder.
            /folders/{folder_id}#add_shared_link:
              put:
                summary: Add shared link to folder
                tags:
                  - Add
                  - Shared
                  - Link
                  - To
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                description: Adds a shared link to a folder.
            /folders/{folder_id}#update_shared_link:
              put:
                summary: Update shared link on folder
                tags:
                  - Update
                  - Shared
                  - Link
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                description: Updates a shared link on a folder.
            /folders/{folder_id}#remove_shared_link:
              put:
                summary: Remove shared link from folder
                tags:
                  - Remove
                  - Shared
                  - Link
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                description: Removes a shared link from a folder.
            /users/{user_id}/folders/0:
              put:
                summary: Transfer owned folders
                tags:
                  - Transfer
                  - Owned
                  - Folders
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Users
                  - User_id
                description: >-
                  Move all of the items (files, folders and workflows) owned by
                  a user into

                  another user's account


                  Only the root folder (`0`) can be transferred.


                  Folders can only be moved across users by users with
                  administrative

                  permissions.


                  All existing shared links and folder-level collaborations are
                  transferred

                  during the operation. Please note that while collaborations at
                  the individual

                  file-level are transferred during the operation, the
                  collaborations are

                  deleted when the original user is deleted.


                  This call will be performed synchronously which might lead to
                  a slow response

                  when the source user has a large number of items in all of its
                  folders.


                  If the destination path has a metadata cascade policy attached
                  to any of

                  the parent folders, a metadata cascade operation will be
                  kicked off

                  asynchronously.


                  There is currently no way to check for when this operation is
                  finished.


                  The destination folder's name will be in the format `{User}'s
                  Files and

                  Folders`, where `{User}` is the display name of the user.


                  To make this API call your application will need to have the
                  "Read and write

                  all files and folders stored in Box" scope enabled.


                  Please make sure the destination user has access to `Relay` or
                  `Relay Lite`,

                  and has access to the files and folders involved in the
                  workflows being

                  transferred.


                  Admins will receive an email when the operation i
    overlays:
      - type: APIs.io Search
        url: overlays/folders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/folders-openapi-api-evangelist-ratings.yml
  - aid: box:box-metadata-cascade-policies-api
    name: Box Metadata Cascade Policies API
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
            title: Box Metadata Cascade Policies API
          paths:
            /metadata_cascade_policies:
              get:
                summary: List metadata cascade policies
                tags:
                  - List
                  - Metadata
                  - Cascade
                  - Policies
                  - Metadata_cascade_policies
                description: >-
                  Retrieves a list of all the metadata cascade policies

                  that are applied to a given folder. This can not be used on
                  the root

                  folder with ID `0`.
              post:
                summary: Create metadata cascade policy
                tags:
                  - Create
                  - Metadata
                  - Cascade
                  - Policy
                  - Metadata_cascade_policies
                description: >-
                  Creates a new metadata cascade policy that applies a given

                  metadata template to a given folder and automatically

                  cascades it down to any files within that folder.


                  In order for the policy to be applied a metadata instance must
                  first

                  be applied to the folder the policy is to be applied to.
            /metadata_cascade_policies/{metadata_cascade_policy_id}:
              get:
                summary: Get metadata cascade policy
                tags:
                  - Get
                  - Metadata
                  - Cascade
                  - Policy
                  - Metadata_cascade_policies
                  - Metadata_cascade_policy_id
                description: >-
                  Retrieve a specific metadata cascade policy assigned to a
                  folder.
              delete:
                summary: Remove metadata cascade policy
                tags:
                  - Remove
                  - Metadata
                  - Cascade
                  - Policy
                  - Metadata_cascade_policies
                  - Metadata_cascade_policy_id
                description: Deletes a metadata cascade policy.
            /metadata_cascade_policies/{metadata_cascade_policy_id}/apply:
              post:
                summary: Force-apply metadata cascade policy to folder
                tags:
                  - Force-apply
                  - Metadata
                  - Cascade
                  - Policy
                  - To
                  - Folder
                  - Metadata_cascade_policies
                  - Metadata_cascade_policy_id
                  - Apply
                description: >-
                  Force the metadata on a folder with a metadata cascade policy
                  to be applied to

                  all of its children. This can be used after creating a new
                  cascade policy to

                  enforce the metadata to be cascaded down to all existing files
                  within 
    overlays:
      - type: APIs.io Search
        url: overlays/metadata-cascade-policies-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/metadata-cascade-policies-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---