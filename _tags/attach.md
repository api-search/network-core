---
name: Attach
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/attach.png
url: https://example.com/apis/attach.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Attach
apis:
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
  - aid: stripe:stripe-payment-method-api
    name: Stripe Payment Method API
    description: >-
      The Payment Methods API allows you to accept a variety of payment methods
      through a single API. A PaymentMethod object contains the payment method
      details to create payments.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/payments/payment-methods
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/payments/payment-methods
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Payment Method API
          paths:
            /v1/payment_method_configurations:
              get:
                description: <p>List payment method configurations</p>
                tags:
                  - V1
                  - Payment_method_configurations
              post:
                description: <p>Creates a payment method configuration</p>
                tags:
                  - V1
                  - Payment_method_configurations
            /v1/payment_method_configurations/{configuration}:
              get:
                description: <p>Retrieve payment method configuration</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
              post:
                description: <p>Update payment method configuration</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
            /v1/payment_method_domains:
              get:
                description: <p>Lists the details of existing payment method domains.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
              post:
                description: <p>Creates a payment method domain.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
            /v1/payment_method_domains/{payment_method_domain}:
              get:
                description: >-
                  <p>Retrieves the details of an existing payment method
                  domain.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
              post:
                description: <p>Updates an existing payment method domain.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
            /v1/payment_method_domains/{payment_method_domain}/validate:
              post:
                description: >-
                  <p>Some payment methods such as Apple Pay require additional
                  steps to verify a domain. If the requirements weren’t
                  satisfied when the domain was created, the payment method will
                  be inactive on the domain.

                  The payment method doesn’t appear in Elements for this domain
                  until it is active.</p>


                  <p>To activate a payment method on an existing payment method
                  domain, complete the required validation steps specific to the
                  payment method, and then validate the payment method domain
                  with this endpoint.</p>


                  <p>Related guides: <a
                  href="/docs/payments/payment-methods/pmd-registration">Payment
                  method domains</a>.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
            /v1/payment_methods:
              get:
                description: >-
                  <p>Returns a list of PaymentMethods for Treasury flows. If you
                  want to list the PaymentMethods attached to a Customer for
                  payments, you should use the <a
                  href="/docs/api/payment_methods/customer_list">List a
                  Customer’s PaymentMethods</a> API instead.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
                  - Payment_methods
              post:
                description: >-
                  <p>Creates a PaymentMethod object. Read the <a
                  href="/docs/stripe-js/reference#stripe-create-payment-method">Stripe.js
                  reference</a> to learn how to create PaymentMethods via
                  Stripe.js.</p>


                  <p>Instead of creating a PaymentMethod directly, we recommend
                  using the <a
                  href="/docs/payments/accept-a-payment">PaymentIntents</a> API
                  to accept a payment immediately or the <a
                  href="/docs/payments/save-and-reuse">SetupIntent</a> API to
                  collect payment method details ahead of a future payment.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
                  - Payment_methods
            /v1/payment_methods/{payment_method}:
              get:
                description: >-
                  <p>Retrieves a PaymentMethod object attached to the
                  StripeAccount. To retrieve a payment method attached to a
                  Customer, you should use <a
                  href="/docs/api/payment_methods/customer">Retrieve a
                  Customer’s PaymentMethods</a></p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
                  - Payment_methods
                  - Payment_method
              post:
                description: >-
                  <p>Updates a PaymentMethod object. A PaymentMethod must be
                  attached a customer to be updated.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
                  - Payment_methods
                  - Payment_method
            /v1/payment_methods/{payment_method}/attach:
              post:
                description: >-
                  <p>Attaches a PaymentMethod object to a Customer.</p>


                  <p>To attach a new PaymentMethod to a customer for future
                  payments, we recommend you use a <a
                  href="/docs/api/setup_intents">SetupIntent</a>

                  or a PaymentIntent with <a
                  href="/docs/api/payment_intents/create#create_payment_intent-setup_future_usage">setup_future_usage</a>.

                  These approaches will perform any necessary steps to set up
                  the PaymentMethod for future payments. Using the
                  <code>/v1/payment_methods/:id/attach</code>

                  endpoint without first using a SetupIntent or PaymentIntent
                  with <code>setup_future_usage</code> does not optimize the
                  PaymentMethod for

                  future use, which makes later declines and payment friction
                  more likely.

                  See <a
                  href="/docs/payments/payment-intents#future-usage">Optimizing
                  cards for future payments</a> for more information about
                  setting up

                  future payments.</p>


                  <p>To use this PaymentMethod as the default for invoice or
                  subscription payments,

                  set <a
                  href="/docs/api/customers/update#update_customer-invoice_settings-default_payment_method"><code>invoice_settings.default_payment_method</code></a>,

                  on the Customer to the PaymentMethod’s ID.</p>
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
                  - Payment_methods
                  - Payment_method
                  - Attach
            /v1/payment_methods/{payment_method}/detach:
              post:
                description: >-
                  <p>Detaches a PaymentMethod object from a Customer. After a
                  PaymentMethod is detached, it can no longer be used for a
                  payment or re-attached to a Cus
                tags:
                  - V1
                  - Payment_method_configurations
                  - Configuration
                  - Payment_method_domains
                  - Payment_method_domain
                  - Validate
                  - Payment_methods
                  - Payment_method
                  - Attach
                  - Deta
    overlays:
      - type: APIs.io Search
        url: overlays/payment-method-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payment-method-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---