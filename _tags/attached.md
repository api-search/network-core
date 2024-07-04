---
name: Attached
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/attached.png
url: https://example.com/apis/attached.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Attached
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
  - name: iot
    description: >-
      <fullname>IoT</fullname> <p>IoT provides secure, bi-directional
      communication between Internet-connected devices (such as sensors,
      actuators, embedded devices, or smart appliances) and the Amazon Web
      Services cloud. You can discover your custom IoT-Data endpoint to
      communicate with, configure rules for data processing and integration with
      other services, organize resources associated with each device (Registry),
      configure logging, and create and manage policies and credentials to
      authenticate devices.</p> <p>The service endpoints that expose this API
      are listed in <a
      href="https://docs.aws.amazon.com/general/latest/gr/iot-core.html">Amazon
      Web Services IoT Core Endpoints and Quotas</a>. You must use the endpoint
      for the region that has the resources you want to access.</p> <p>The
      service name used by <a
      href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Amazon
      Web Services Signature Version 4</a> to sign the request is:
      <i>execute-api</i>.</p> <p>For more information about how IoT works, see
      the <a
      href="https://docs.aws.amazon.com/iot/latest/developerguide/aws-iot-how-it-works.html">Developer
      Guide</a>.</p> <p>For information about how to use the credentials
      provider for IoT, see <a
      href="https://docs.aws.amazon.com/iot/latest/developerguide/authorizing-direct-aws.html">Authorizing
      Direct Calls to Amazon Web Services Services</a>.</p>
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
            title: iot
          paths:
            /accept-certificate-transfer/{certificateId}:
              PATCH:
                summary: AcceptCertificateTransfer
                description: >-
                  <p>Accepts a pending certificate transfer. The default state
                  of the certificate is INACTIVE.</p> <p>To check for pending
                  certificate transfers, call <a>ListCertificates</a> to
                  enumerate your certificates.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AcceptCertificateTransfer</a>
                  action.</p>
                tags:
                  - Accept
                  - Certificates
                  - Transfers
                  - Identifiers
            /billing-groups/addThingToBillingGroup:
              PUT:
                summary: AddThingToBillingGroup
                description: >-
                  <p>Adds a thing to a billing group.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AddThingToBillingGroup</a>
                  action.</p>
                tags:
                  - Add
                  - Things
                  - To
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
            /thing-groups/addThingToThingGroup:
              PUT:
                summary: AddThingToThingGroup
                description: >-
                  <p>Adds a thing to a thing group.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AddThingToThingGroup</a>
                  action.</p>
                tags:
                  - Add
                  - Things
                  - To
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
            /jobs/{jobId}/targets:
              POST:
                summary: AssociateTargetsWithJob
                description: >-
                  <p>Associates a group with a continuous job. The following
                  criteria must be met: </p> <ul> <li> <p>The job must have been
                  created with the <code>targetSelection</code> field set to
                  "CONTINUOUS".</p> </li> <li> <p>The job status must currently
                  be "IN_PROGRESS".</p> </li> <li> <p>The total number of
                  targets associated with a job must not exceed 100.</p> </li>
                  </ul> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AssociateTargetsWithJob</a>
                  action.</p>
                tags:
                  - Associate
                  - Targets
                  - With
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
            /target-policies/{policyName}:
              POST:
                summary: DetachPolicy
                description: >-
                  <p>Detaches a policy from the specified target.</p> <note>
                  <p>Because of the distributed nature of Amazon Web Services,
                  it can take up to five minutes after a policy is detached
                  before it's ready to be deleted.</p> </note> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DetachPolicy</a>
                  action.</p>
                tags:
                  - Detach
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
            /principal-policies/{policyName}:
              DELETE:
                summary: DetachPrincipalPolicy
                description: >-
                  <p>Removes the specified policy from the specified
                  certificate.</p> <p> <b>Note:</b> This action is deprecated
                  and works as expected for backward compatibility, but we won't
                  add enhancements. Use <a>DetachPolicy</a> instead.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DetachPrincipalPolicy</a>
                  action.</p>
                tags:
                  - Detach
                  - Principals
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
            /security-profiles/{securityProfileName}/targets:
              GET:
                summary: ListTargetsForSecurityProfile
                description: >-
                  <p>Lists the targets (thing groups) associated with a given
                  Device Defender security profile.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListTargetsForSecurityProfile</a>
                  action.</p>
                tags:
                  - Lists
                  - Targets
                  - For
                  - Security
                  - Profiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
            /things/{thingName}/principals:
              GET:
                summary: ListThingPrincipals
                description: >-
                  <p>Lists the principals associated with the specified thing. A
                  principal can be X.509 certificates, IAM users, groups, and
                  roles, Amazon Cognito identities or federated identities.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingPrincipals</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Principals
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
            /audit/mitigationactions/tasks/{taskId}/cancel:
              PUT:
                summary: CancelAuditMitigationActionsTask
                description: >-
                  <p>Cancels a mitigation action task that is in progress. If
                  the task is not in progress, an InvalidRequestException
                  occurs.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelAuditMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Cancel
                  - Audit
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /audit/tasks/{taskId}/cancel:
              PUT:
                summary: CancelAuditTask
                description: >-
                  <p>Cancels an audit that is in progress. The audit can be
                  either scheduled or on demand. If the audit isn't in progress,
                  an "InvalidRequestException" occurs.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelAuditTask</a>
                  action.</p>
                tags:
                  - Cancel
                  - Audit
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /cancel-certificate-transfer/{certificateId}:
              PATCH:
                summary: CancelCertificateTransfer
                description: >-
                  <p>Cancels a pending transfer for the specified
                  certificate.</p> <p> <b>Note</b> Only the transfer source
                  account can use this operation to cancel a transfer. (Transfer
                  destinations can use <a>RejectCertificateTransfer</a>
                  instead.) After transfer, IoT returns the certificate to the
                  source account in the INACTIVE state. After the destination
                  account has accepted the transfer, the transfer cannot be
                  cancelled.</p> <p>After a certificate transfer is cancelled,
                  the status of the certificate changes from PENDING_TRANSFER to
                  INACTIVE.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelCertificateTransfer</a>
                  action.</p>
                tags:
                  - Cancel
                  - Certificates
                  - Transfers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /detect/mitigationactions/tasks/{taskId}/cancel:
              PUT:
                summary: CancelDetectMitigationActionsTask
                description: >-
                  <p> Cancels a Device Defender ML Detect mitigation action.
                  </p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelDetectMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Cancel
                  - Detect
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /jobs/{jobId}/cancel:
              PUT:
                summary: CancelJob
                description: >-
                  <p>Cancels a job.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelJob</a>
                  action.</p>
                tags:
                  - Cancel
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /things/{thingName}/jobs/{jobId}/cancel:
              PUT:
                summary: CancelJobExecution
                description: >-
                  <p>Cancels the execution of a job for a given thing.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelJobExecution</a>
                  action.</p>
                tags:
                  - Cancel
                  - Jobs
                  - Execution
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
            /default-authorizer:
              POST:
                summary: SetDefaultAuthorizer
                description: >-
                  <p>Sets the default authorizer. This will be used if a
                  websocket connection is made without specifying an
                  authorizer.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetDefaultAuthorizer</a>
                  action.</p>
                tags:
                  - Sets
                  - Default
                  - Authorizer
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
            /confirmdestination/{confirmationToken+}:
              GET:
                summary: ConfirmTopicRuleDestination
                description: >-
                  <p>Confirms a topic rule destination. When you create a rule
                  requiring a destination, IoT sends a confirmation message to
                  the endpoint or base address you specify. The message includes
                  a token which you pass back when calling
                  <code>ConfirmTopicRuleDestination</code> to confirm that you
                  own or have access to the endpoint.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ConfirmTopicRuleDestination</a>
                  action.</p>
                tags:
                  - Confirm
                  - Topics
                  - Rules
                  - Destinations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
            /audit/suppressions/create:
              POST:
                summary: CreateAuditSuppression
                description: >-
                  <p> Creates a Device Defender audit suppression. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CreateAuditSuppression</a>
                  action.</p>
                tags:
                  - Create
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
            /authorizer/{authorizerName}:
              PUT:
                summary: UpdateAuthorizer
                description: >-
                  <p>Updates an authorizer.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateAuthorizer</a>
                  action.</p>
                tags:
                  - Update
                  - Authorizer
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
            /billing-groups/{billingGroupName}:
              PATCH:
                summary: UpdateBillingGroup
                description: >-
                  <p>Updates information about the billing group.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateBillingGroup</a>
                  action.</p>
                tags:
                  - Update
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
            /certificates:
              GET:
                summary: ListCertificates
                description: >-
                  <p>Lists the certificates registered in your Amazon Web
                  Services account.</p> <p>The results are paginated with a
                  default page size of 25. You can use the returned marker to
                  retrieve additional results.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCertificates</a>
                  action.</p>
                tags:
                  - Lists
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
            /certificate-providers/{certificateProviderName}:
              PUT:
                summary: UpdateCertificateProvider
                description: >-
                  <p>Updates a certificate provider.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCertificateProvider</a>
                  action. </p>
                tags:
                  - Update
                  - Certificates
                  - Providers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
            /custom-metric/{metricName}:
              PATCH:
                summary: UpdateCustomMetric
                description: >-
                  <p>Updates a Device Defender detect custom metric. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCustomMetric</a>
                  action.</p>
                tags:
                  - Update
                  - Custom
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
            /dimensions/{name}:
              PATCH:
                summary: UpdateDimension
                description: >-
                  <p>Updates the definition for a dimension. You cannot change
                  the type of a dimension after it is created (you can delete it
                  and recreate it).</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateDimension</a>
                  action.</p>
                tags:
                  - Update
                  - Dimensions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
            /domainConfigurations/{domainConfigurationName}:
              PUT:
                summary: UpdateDomainConfiguration
                description: >-
                  <p>Updates values stored in the domain configuration. Domain
                  configurations for default endpoints can't be updated.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateDomainConfiguration</a>
                  action.</p>
                tags:
                  - Update
                  - Domains
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /dynamic-thing-groups/{thingGroupName}:
              PATCH:
                summary: UpdateDynamicThingGroup
                description: >-
                  <p>Updates a dynamic thing group.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateDynamicThingGroup</a>
                  action.</p>
                tags:
                  - Update
                  - Dynamic
                  - Things
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /fleet-metric/{metricName}:
              PATCH:
                summary: UpdateFleetMetric
                description: >-
                  <p>Updates the data for a fleet metric.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateFleetMetric</a>
                  action.</p>
                tags:
                  - Update
                  - Fleets
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /jobs/{jobId}:
              PATCH:
                summary: UpdateJob
                description: >-
                  <p>Updates supported fields of the specified job.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateJob</a>
                  action.</p>
                tags:
                  - Update
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /job-templates/{jobTemplateId}:
              GET:
                summary: DescribeJobTemplate
                description: <p>Returns information about a job template.</p>
                tags:
                  - Describe
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
            /keys-and-certificate:
              POST:
                summary: CreateKeysAndCertificate
                description: >-
                  <p>Creates a 2048-bit RSA key pair and issues an X.509
                  certificate using the issued public key. You can also call
                  <code>CreateKeysAndCertificate</code> over MQTT from a device,
                  for more information, see <a
                  href="https://docs.aws.amazon.com/iot/latest/developerguide/provision-wo-cert.html#provision-mqtt-api">Provisioning
                  MQTT API</a>.</p> <p> <b>Note</b> This is the only time IoT
                  issues the private key for this certificate, so it is
                  important to keep it in a secure location.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CreateKeysAndCertificate</a>
                  action.</p>
                tags:
                  - Create
                  - Keys
                  - And
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
            /mitigationactions/actions/{actionName}:
              PATCH:
                summary: UpdateMitigationAction
                description: >-
                  <p>Updates the definition for the specified mitigation
                  action.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateMitigationAction</a>
                  action.</p>
                tags:
                  - Update
                  - Mitigation
                  - Actions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
            /otaUpdates/{otaUpdateId}:
              GET:
                summary: GetOTAUpdate
                description: >-
                  <p>Gets an OTA update.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetOTAUpdate</a>
                  action.</p>
                tags:
                  - Get
                  - Update
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
            /packages/{packageName}:
              PATCH:
                summary: UpdatePackage
                description: >-
                  <p>Updates the supported fields for a specific software
                  package.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdatePackage</a>
                  and <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetIndexingConfiguration</a>
                  actions.</p>
                tags:
                  - Update
                  - Packages
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
            /packages/{packageName}/versions/{versionName}:
              PATCH:
                summary: UpdatePackageVersion
                description: >-
                  <p>Updates the supported fields for a specific package
                  version.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdatePackageVersion</a>
                  and <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetIndexingConfiguration</a>
                  actions.</p>
                tags:
                  - Update
                  - Packages
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
            /policies/{policyName}:
              GET:
                summary: GetPolicy
                description: >-
                  <p>Gets information about the specified policy with the policy
                  document of the default version.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetPolicy</a>
                  action.</p>
                tags:
                  - Get
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
            /policies/{policyName}/version:
              GET:
                summary: ListPolicyVersions
                description: >-
                  <p>Lists the versions of the specified policy and identifies
                  the default version.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPolicyVersions</a>
                  action.</p>
                tags:
                  - Lists
                  - Policies
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
            /provisioning-templates/{templateName}/provisioning-claim:
              POST:
                summary: CreateProvisioningClaim
                description: >-
                  <p>Creates a provisioning claim.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CreateProvisioningClaim</a>
                  action.</p>
                tags:
                  - Create
                  - Provisioning
                  - Claim
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
            /provisioning-templates:
              GET:
                summary: ListProvisioningTemplates
                description: >-
                  <p>Lists the provisioning templates in your Amazon Web
                  Services account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListProvisioningTemplates</a>
                  action.</p>
                tags:
                  - Lists
                  - Provisioning
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
            /provisioning-templates/{templateName}/versions:
              GET:
                summary: ListProvisioningTemplateVersions
                description: >-
                  <p>A list of provisioning template versions.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListProvisioningTemplateVersions</a>
                  action.</p>
                tags:
                  - Lists
                  - Provisioning
                  - Templates
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
            /role-aliases/{roleAlias}:
              PUT:
                summary: UpdateRoleAlias
                description: >-
                  <p>Updates a role alias.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateRoleAlias</a>
                  action.</p>
                tags:
                  - Update
                  - Roles
                  - Alias
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /audit/scheduledaudits/{scheduledAuditName}:
              PATCH:
                summary: UpdateScheduledAudit
                description: >-
                  <p>Updates a scheduled audit, including which checks are
                  performed and how often the audit takes place.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateScheduledAudit</a>
                  action.</p>
                tags:
                  - Update
                  - Scheduled
                  - Audit
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /security-profiles/{securityProfileName}:
              PATCH:
                summary: UpdateSecurityProfile
                description: >-
                  <p>Updates a Device Defender security profile.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateSecurityProfile</a>
                  action.</p>
                tags:
                  - Update
                  - Security
                  - Profiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /streams/{streamId}:
              PUT:
                summary: UpdateStream
                description: >-
                  <p>Updates an existing stream. The stream version will be
                  incremented by one.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateStream</a>
                  action.</p>
                tags:
                  - Update
                  - Stream
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /things/{thingName}:
              PATCH:
                summary: UpdateThing
                description: >-
                  <p>Updates the data for a thing.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateThing</a>
                  action.</p>
                tags:
                  - Update
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /thing-groups/{thingGroupName}:
              PATCH:
                summary: UpdateThingGroup
                description: >-
                  <p>Update a thing group.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateThingGroup</a>
                  action.</p>
                tags:
                  - Update
                  - Things
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /thing-types/{thingTypeName}:
              GET:
                summary: DescribeThingType
                description: >-
                  <p>Gets information about the specified thing type.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeThingType</a>
                  action.</p>
                tags:
                  - Describe
                  - Things
                  - Types
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
            /rules/{ruleName}:
              PATCH:
                summary: ReplaceTopicRule
                description: >-
                  <p>Replaces the rule. You must specify all parameters for the
                  new rule. Creating rules is an administrator-level action. Any
                  user who has permission to create rules will be able to access
                  data processed by the rule.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ReplaceTopicRule</a>
                  action.</p>
                tags:
                  - Replace
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
            /destinations:
              PATCH:
                summary: UpdateTopicRuleDestination
                description: >-
                  <p>Updates a topic rule destination. You use this to change
                  the status, endpoint URL, or confirmation URL of the
                  destination.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateTopicRuleDestination</a>
                  action.</p>
                tags:
                  - Update
                  - Topics
                  - Rules
                  - Destinations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
            /audit/configuration:
              PATCH:
                summary: UpdateAccountAuditConfiguration
                description: >-
                  <p>Configures or reconfigures the Device Defender audit
                  settings for this account. Settings include how audit
                  notifications are sent and which audit checks are enabled or
                  disabled.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateAccountAuditConfiguration</a>
                  action.</p>
                tags:
                  - Update
                  - Account
                  - Audit
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
            /audit/suppressions/delete:
              POST:
                summary: DeleteAuditSuppression
                description: >-
                  <p> Deletes a Device Defender audit suppression. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DeleteAuditSuppression</a>
                  action.</p>
                tags:
                  - Delete
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
            /cacertificate/{caCertificateId}:
              PUT:
                summary: UpdateCACertificate
                description: >-
                  <p>Updates a registered CA certificate.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCACertificate</a>
                  action.</p>
                tags:
                  - Update
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
            /certificates/{certificateId}:
              PUT:
                summary: UpdateCertificate
                description: >-
                  <p>Updates the status of the specified certificate. This
                  operation is idempotent.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCertificate</a>
                  action.</p> <p>Certificates must be in the ACTIVE state to
                  authenticate devices that use a certificate to connect to
                  IoT.</p> <p>Within a few minutes of updating a certificate
                  from the ACTIVE state to any other state, IoT disconnects all
                  devices that used that certificate to connect. Devices cannot
                  use a certificate that is not in the ACTIVE state to
                  reconnect.</p>
                tags:
                  - Update
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
            /things/{thingName}/jobs/{jobId}/executionNumber/{executionNumber}:
              DELETE:
                summary: DeleteJobExecution
                description: >-
                  <p>Deletes a job execution.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DeleteJobExecution</a>
                  action.</p>
                tags:
                  - Delete
                  - Jobs
                  - Execution
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
            /policies/{policyName}/version/{policyVersionId}:
              PATCH:
                summary: SetDefaultPolicyVersion
                description: >-
                  <p>Sets the specified version of the specified policy as the
                  policy's default (operative) version. This action affects all
                  certificates to which the policy is attached. To list the
                  principals the policy is attached to, use the
                  <a>ListPrincipalPolicies</a> action.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetDefaultPolicyVersion</a>
                  action.</p>
                tags:
                  - Sets
                  - Default
                  - Policies
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
            /provisioning-templates/{templateName}:
              PATCH:
                summary: UpdateProvisioningTemplate
                description: >-
                  <p>Updates a provisioning template.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateProvisioningTemplate</a>
                  action.</p>
                tags:
                  - Update
                  - Provisioning
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
            /provisioning-templates/{templateName}/versions/{versionId}:
              GET:
                summary: DescribeProvisioningTemplateVersion
                description: >-
                  <p>Returns information about a provisioning template
                  version.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeProvisioningTemplateVersion</a>
                  action.</p>
                tags:
                  - Describe
                  - Provisioning
                  - Templates
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
            /registrationcode:
              GET:
                summary: GetRegistrationCode
                description: >-
                  <p>Gets a registration code used to register a CA certificate
                  with IoT.</p> <p>IoT will create a registration code as part
                  of this API call if the registration code doesn't exist or has
                  been deleted. If you already have a registration code, this
                  API call will return the same registration code.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetRegistrationCode</a>
                  action.</p>
                tags:
                  - Get
                  - Registrations
                  - Code
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
            /destinations/{arn+}:
              GET:
                summary: GetTopicRuleDestination
                description: >-
                  <p>Gets information about a topic rule destination.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetTopicRuleDestination</a>
                  action.</p>
                tags:
                  - Get
                  - Topics
                  - Rules
                  - Destinations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
            /v2LoggingLevel:
              POST:
                summary: SetV2LoggingLevel
                description: >-
                  <p>Sets the logging level.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetV2LoggingLevel</a>
                  action.</p>
                tags:
                  - Sets
                  - V2
                  - Logging
                  - Levels
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
            /thing-types/{thingTypeName}/deprecate:
              POST:
                summary: DeprecateThingType
                description: >-
                  <p>Deprecates a thing type. You can not associate new things
                  with deprecated thing type.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DeprecateThingType</a>
                  action.</p>
                tags:
                  - Deprecate
                  - Things
                  - Types
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
            /audit/findings/{findingId}:
              GET:
                summary: DescribeAuditFinding
                description: >-
                  <p>Gets information about a single audit finding. Properties
                  include the reason for noncompliance, the severity of the
                  issue, and the start time when the audit that returned the
                  finding.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeAuditFinding</a>
                  action.</p>
                tags:
                  - Describe
                  - Audit
                  - Findings
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
            /audit/mitigationactions/tasks/{taskId}:
              POST:
                summary: StartAuditMitigationActionsTask
                description: >-
                  <p>Starts a task that applies a set of mitigation actions to
                  the specified target.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartAuditMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Start
                  - Audit
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
            /audit/suppressions/describe:
              POST:
                summary: DescribeAuditSuppression
                description: >-
                  <p> Gets information about a Device Defender audit
                  suppression. </p>
                tags:
                  - Describe
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
            /audit/tasks/{taskId}:
              GET:
                summary: DescribeAuditTask
                description: >-
                  <p>Gets information about a Device Defender audit.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeAuditTask</a>
                  action.</p>
                tags:
                  - Describe
                  - Audit
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
            /detect/mitigationactions/tasks/{taskId}:
              PUT:
                summary: StartDetectMitigationActionsTask
                description: >-
                  <p> Starts a Device Defender ML Detect mitigation actions
                  task. </p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartDetectMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Start
                  - Detect
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
            /endpoint:
              GET:
                summary: DescribeEndpoint
                description: >-
                  <p>Returns or creates a unique endpoint specific to the Amazon
                  Web Services account making the call.</p> <note> <p>The first
                  time <code>DescribeEndpoint</code> is called, an endpoint is
                  created. All subsequent calls to <code>DescribeEndpoint</code>
                  return the same endpoint.</p> </note> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeEndpoint</a>
                  action.</p>
                tags:
                  - Describe
                  - Endpoints
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
            /event-configurations:
              PATCH:
                summary: UpdateEventConfigurations
                description: >-
                  <p>Updates the event configurations.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateEventConfigurations</a>
                  action.</p>
                tags:
                  - Update
                  - Events
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /indices/{indexName}:
              GET:
                summary: DescribeIndex
                description: >-
                  <p>Describes a search index.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeIndex</a>
                  action.</p>
                tags:
                  - Describe
                  - Index
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /things/{thingName}/jobs/{jobId}:
              GET:
                summary: DescribeJobExecution
                description: >-
                  <p>Describes a job execution.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeJobExecution</a>
                  action.</p>
                tags:
                  - Describe
                  - Jobs
                  - Execution
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /managed-job-templates/{templateName}:
              GET:
                summary: DescribeManagedJobTemplate
                description: <p>View details of a managed job template.</p>
                tags:
                  - Describe
                  - Managed
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /thing-registration-tasks/{taskId}:
              GET:
                summary: DescribeThingRegistrationTask
                description: >-
                  <p>Describes a bulk thing provisioning task.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeThingRegistrationTask</a>
                  action.</p>
                tags:
                  - Describe
                  - Things
                  - Registrations
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /rules/{ruleName}/disable:
              POST:
                summary: DisableTopicRule
                description: >-
                  <p>Disables the rule.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DisableTopicRule</a>
                  action.</p>
                tags:
                  - Disable
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
            /rules/{ruleName}/enable:
              POST:
                summary: EnableTopicRule
                description: >-
                  <p>Enables the rule.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">EnableTopicRule</a>
                  action.</p>
                tags:
                  - Enable
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
            /behavior-model-training/summaries:
              GET:
                summary: GetBehaviorModelTrainingSummaries
                description: >-
                  <p> Returns a Device Defender's ML Detect Security Profile
                  training model's status. </p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetBehaviorModelTrainingSummaries</a>
                  action.</p>
                tags:
                  - Get
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
            /indices/buckets:
              POST:
                summary: GetBucketsAggregation
                description: >-
                  <p>Aggregates on indexed data with search queries pertaining
                  to particular fields. </p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetBucketsAggregation</a>
                  action.</p>
                tags:
                  - Get
                  - Buckets
                  - Aggregation
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
            /indices/cardinality:
              POST:
                summary: GetCardinality
                description: >-
                  <p>Returns the approximate count of unique values that match
                  the query.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetCardinality</a>
                  action.</p>
                tags:
                  - Get
                  - Cardinality
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
            /effective-policies:
              POST:
                summary: GetEffectivePolicies
                description: >-
                  <p>Gets a list of the policies that have an effect on the
                  authorization behavior of the specified device when it
                  connects to the IoT device gateway.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetEffectivePolicies</a>
                  action.</p>
                tags:
                  - Get
                  - Effective
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
            /indexing/config:
              POST:
                summary: UpdateIndexingConfiguration
                description: >-
                  <p>Updates the search configuration.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateIndexingConfiguration</a>
                  action.</p>
                tags:
                  - Update
                  - Indexing
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
            /jobs/{jobId}/job-document:
              GET:
                summary: GetJobDocument
                description: >-
                  <p>Gets a job document.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetJobDocument</a>
                  action.</p>
                tags:
                  - Get
                  - Jobs
                  - Document
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
            /loggingOptions:
              POST:
                summary: SetLoggingOptions
                description: >-
                  <p>Sets the logging options.</p> <p>NOTE: use of this command
                  is not recommended. Use <code>SetV2LoggingOptions</code>
                  instead.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetLoggingOptions</a>
                  action.</p>
                tags:
                  - Sets
                  - Logging
                  - Options
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
            /package-configuration:
              PATCH:
                summary: UpdatePackageConfiguration
                description: >-
                  <p>Updates the software package configuration.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdatePackageConfiguration</a>
                  and <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html">iam:PassRole</a>
                  actions.</p>
                tags:
                  - Update
                  - Packages
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
            /indices/percentiles:
              POST:
                summary: GetPercentiles
                description: >-
                  <p>Groups the aggregated values that match the query into
                  percentile groupings. The default percentile groupings are:
                  1,5,25,50,75,95,99, although you can specify your own when you
                  call <code>GetPercentiles</code>. This function returns a
                  value for each percentile group specified (or the default
                  percentile groupings). The percentile group "1" contains the
                  aggregated field value that occurs in approximately one
                  percent of the values that match the query. The percentile
                  group "5" contains the aggregated field value that occurs in
                  approximately five percent of the values that match the query,
                  and so on. The result is an approximation, the more values
                  that match the query, the more accurate the percentile
                  values.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetPercentiles</a>
                  action.</p>
                tags:
                  - Get
                  - Percentiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
            /indices/statistics:
              POST:
                summary: GetStatistics
                description: >-
                  <p>Returns the count, average, sum, minimum, maximum, sum of
                  squares, variance, and standard deviation for the specified
                  aggregated field. If the aggregation field is of type
                  <code>String</code>, only the count statistic is returned.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetStatistics</a>
                  action.</p>
                tags:
                  - Get
                  - Statistics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
            /v2LoggingOptions:
              POST:
                summary: SetV2LoggingOptions
                description: >-
                  <p>Sets the logging options for the V2 logging service.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetV2LoggingOptions</a>
                  action.</p>
                tags:
                  - Sets
                  - V2
                  - Logging
                  - Options
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
            /active-violations:
              GET:
                summary: ListActiveViolations
                description: >-
                  <p>Lists the active violations for a given Device Defender
                  security profile.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListActiveViolations</a>
                  action.</p>
                tags:
                  - Lists
                  - Active
                  - Violations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
            /attached-policies/{target}:
              POST:
                summary: ListAttachedPolicies
                description: >-
                  <p>Lists the policies attached to the specified thing
                  group.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAttachedPolicies</a>
                  action.</p>
                tags:
                  - Lists
                  - Attached
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
            /audit/findings:
              POST:
                summary: ListAuditFindings
                description: >-
                  <p>Lists the findings (results) of a Device Defender audit or
                  of the audits performed during a specified time period.
                  (Findings are retained for 90 days.)</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditFindings</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Findings
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
            /audit/mitigationactions/executions:
              GET:
                summary: ListAuditMitigationActionsExecutions
                description: >-
                  <p>Gets the status of audit mitigation action tasks that were
                  executed.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditMitigationActionsExecutions</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Mitigation
                  - Actions
                  - Executions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
            /audit/mitigationactions/tasks:
              GET:
                summary: ListAuditMitigationActionsTasks
                description: >-
                  <p>Gets a list of audit mitigation action tasks that match the
                  specified filters.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditMitigationActionsTasks</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
            /audit/suppressions/list:
              POST:
                summary: ListAuditSuppressions
                description: >-
                  <p> Lists your Device Defender audit listings. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditSuppressions</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
            /audit/tasks:
              POST:
                summary: StartOnDemandAuditTask
                description: >-
                  <p>Starts an on-demand Device Defender audit.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartOnDemandAuditTask</a>
                  action.</p>
                tags:
                  - Start
                  - 'On'
                  - Demand
                  - Audit
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
            /authorizers/:
              GET:
                summary: ListAuthorizers
                description: >-
                  <p>Lists the authorizers registered in your account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuthorizers</a>
                  action.</p>
                tags:
                  - Lists
                  - Authorizers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
            /billing-groups:
              GET:
                summary: ListBillingGroups
                description: >-
                  <p>Lists the billing groups you have created.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListBillingGroups</a>
                  action.</p>
                tags:
                  - Lists
                  - Billing
                  - Groups
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
            /cacertificates:
              GET:
                summary: ListCACertificates
                description: >-
                  <p>Lists the CA certificates registered for your Amazon Web
                  Services account.</p> <p>The results are paginated with a
                  default page size of 25. You can use the returned marker to
                  retrieve additional results.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCACertificates</a>
                  action.</p>
                tags:
                  - Lists
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
            /certificate-providers/:
              GET:
                summary: ListCertificateProviders
                description: >-
                  <p>Lists all your certificate providers in your Amazon Web
                  Services account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCertificateProviders</a>
                  action. </p>
                tags:
                  - Lists
                  - Certificates
                  - Providers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
            /certificates-by-ca/{caCertificateId}:
              GET:
                summary: ListCertificatesByCA
                description: >-
                  <p>List the device certificates signed by the specified CA
                  certificate.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCertificatesByCA</a>
                  action.</p>
                tags:
                  - Lists
                  - Certificates
                  - By
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
            /custom-metrics:
              GET:
                summary: ListCustomMetrics
                description: >-
                  <p> Lists your Device Defender detect custom metrics. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCustomMetrics</a>
                  action.</p>
                tags:
                  - Lists
                  - Custom
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
            /detect/mitigationactions/executions:
              GET:
                summary: ListDetectMitigationActionsExecutions
                description: >-
                  <p> Lists mitigation actions executions for a Device Defender
                  ML Detect Security Profile. </p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDetectMitigationActionsExecutions</a>
                  action.</p>
                tags:
                  - Lists
                  - Detect
                  - Mitigation
                  - Actions
                  - Executions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /detect/mitigationactions/tasks:
              GET:
                summary: ListDetectMitigationActionsTasks
                description: >-
                  <p> List of Device Defender ML Detect mitigation actions
                  tasks. </p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDetectMitigationActionsTasks</a>
                  action.</p>
                tags:
                  - Lists
                  - Detect
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /dimensions:
              GET:
                summary: ListDimensions
                description: >-
                  <p>List the set of dimensions that are defined for your Amazon
                  Web Services accounts.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDimensions</a>
                  action.</p>
                tags:
                  - Lists
                  - Dimensions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /domainConfigurations:
              GET:
                summary: ListDomainConfigurations
                description: >-
                  <p>Gets a list of domain configurations for the user. This
                  list is sorted alphabetically by domain configuration
                  name.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDomainConfigurations</a>
                  action.</p>
                tags:
                  - Lists
                  - Domains
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /fleet-metrics:
              GET:
                summary: ListFleetMetrics
                description: >-
                  <p>Lists all your fleet metrics. </p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListFleetMetrics</a>
                  action.</p>
                tags:
                  - Lists
                  - Fleets
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
            /indices:
              GET:
                summary: ListIndices
                description: >-
                  <p>Lists the search indices.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListIndices</a>
                  action.</p>
                tags:
                  - Lists
                  - Indices
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
            /jobs/{jobId}/things:
              GET:
                summary: ListJobExecutionsForJob
                description: >-
                  <p>Lists the job executions for a job.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobExecutionsForJob</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Executions
                  - For
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /things/{thingName}/jobs:
              GET:
                summary: ListJobExecutionsForThing
                description: >-
                  <p>Lists the job executions for the specified thing.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobExecutionsForThing</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Executions
                  - For
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /job-templates:
              GET:
                summary: ListJobTemplates
                description: >-
                  <p>Returns a list of job templates.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobTemplates</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /jobs:
              GET:
                summary: ListJobs
                description: >-
                  <p>Lists jobs.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobs</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /managed-job-templates:
              GET:
                summary: ListManagedJobTemplates
                description: <p>Returns a list of managed job templates.</p>
                tags:
                  - Lists
                  - Managed
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
            /metric-values:
              GET:
                summary: ListMetricValues
                description: >-
                  <p>Lists the values reported for an IoT Device Defender metric
                  (device-side metric, cloud-side metric, or custom metric) by
                  the given thing during the specified time period.</p>
                tags:
                  - Lists
                  - Metrics
                  - Values
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
            /mitigationactions/actions:
              GET:
                summary: ListMitigationActions
                description: >-
                  <p>Gets a list of all mitigation actions that match the
                  specified filter criteria.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListMitigationActions</a>
                  action.</p>
                tags:
                  - Lists
                  - Mitigation
                  - Actions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
            /otaUpdates:
              GET:
                summary: ListOTAUpdates
                description: >-
                  <p>Lists OTA updates.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListOTAUpdates</a>
                  action.</p>
                tags:
                  - Lists
                  - Updates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
            /certificates-out-going:
              GET:
                summary: ListOutgoingCertificates
                description: >-
                  <p>Lists certificates that are being transferred but not yet
                  accepted.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListOutgoingCertificates</a>
                  action.</p>
                tags:
                  - Lists
                  - Outgoing
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
            /packages/{packageName}/versions:
              GET:
                summary: ListPackageVersions
                description: >-
                  <p>Lists the software package versions associated to the
                  account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPackageVersions</a>
                  action.</p>
                tags:
                  - Lists
                  - Packages
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
            /packages:
              GET:
                summary: ListPackages
                description: >-
                  <p>Lists the software packages associated to the account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPackages</a>
                  action.</p>
                tags:
                  - Lists
                  - Packages
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
            /policies:
              GET:
                summary: ListPolicies
                description: >-
                  <p>Lists your policies.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPolicies</a>
                  action.</p>
                tags:
                  - Lists
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
            /policy-principals:
              GET:
                summary: ListPolicyPrincipals
                description: >-
                  <p>Lists the principals associated with the specified
                  policy.</p> <p> <b>Note:</b> This action is deprecated and
                  works as expected for backward compatibility, but we won't add
                  enhancements. Use <a>ListTargetsForPolicy</a> instead.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPolicyPrincipals</a>
                  action.</p>
                tags:
                  - Lists
                  - Policies
                  - Principals
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
            /principal-policies:
              GET:
                summary: ListPrincipalPolicies
                description: >-
                  <p>Lists the policies attached to the specified principal. If
                  you use an Cognito identity, the ID must be in <a
                  href="https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/API_GetCredentialsForIdentity.html#API_GetCredentialsForIdentity_RequestSyntax">AmazonCognito
                  Identity format</a>.</p> <p> <b>Note:</b> This action is
                  deprecated and works as expected for backward compatibility,
                  but we won't add enhancements. Use <a>ListAttachedPolicies</a>
                  instead.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPrincipalPolicies</a>
                  action.</p>
                tags:
                  - Lists
                  - Principals
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
            /principals/things:
              GET:
                summary: ListPrincipalThings
                description: >-
                  <p>Lists the things associated with the specified principal. A
                  principal can be X.509 certificates, IAM users, groups, and
                  roles, Amazon Cognito identities or federated identities. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPrincipalThings</a>
                  action.</p>
                tags:
                  - Lists
                  - Principals
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
            /audit/relatedResources:
              GET:
                summary: ListRelatedResourcesForAuditFinding
                description: >-
                  <p>The related resources of an Audit finding. The following
                  resources can be returned from calling this API:</p> <ul> <li>
                  <p>DEVICE_CERTIFICATE</p> </li> <li> <p>CA_CERTIFICATE</p>
                  </li> <li> <p>IOT_POLICY</p> </li> <li>
                  <p>COGNITO_IDENTITY_POOL</p> </li> <li> <p>CLIENT_ID</p> </li>
                  <li> <p>ACCOUNT_SETTINGS</p> </li> <li> <p>ROLE_ALIAS</p>
                  </li> <li> <p>IAM_ROLE</p> </li> <li>
                  <p>ISSUER_CERTIFICATE</p> </li> </ul> <note> <p>This API is
                  similar to DescribeAuditFinding's <a
                  href="https://docs.aws.amazon.com/iot/latest/apireference/API_DescribeAuditFinding.html">RelatedResources</a>
                  but provides pagination and is not limited to 10 resources.
                  When calling <a
                  href="https://docs.aws.amazon.com/iot/latest/apireference/API_DescribeAuditFinding.html">DescribeAuditFinding</a>
                  for the intermediate CA revoked for active device certificates
                  check, RelatedResources will not be populated. You must use
                  this API, ListRelatedResourcesForAuditFinding, to list the
                  certificates.</p> </note>
                tags:
                  - Lists
                  - Related
                  - Resources
                  - For
                  - Audit
                  - Findings
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
            /role-aliases:
              GET:
                summary: ListRoleAliases
                description: >-
                  <p>Lists the role aliases registered in your account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListRoleAliases</a>
                  action.</p>
                tags:
                  - Lists
                  - Roles
                  - Aliases
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
            /audit/scheduledaudits:
              GET:
                summary: ListScheduledAudits
                description: >-
                  <p>Lists all of your scheduled audits.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListScheduledAudits</a>
                  action.</p>
                tags:
                  - Lists
                  - Scheduled
                  - Audits
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
            /security-profiles:
              GET:
                summary: ListSecurityProfiles
                description: >-
                  <p>Lists the Device Defender security profiles you've created.
                  You can filter security profiles by dimension or custom
                  metric.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListSecurityProfiles</a>
                  action.</p> <note> <p> <code>dimensionName</code> and
                  <code>metricName</code> cannot be used in the same
                  request.</p> </note>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
            /security-profiles-for-target:
              GET:
                summary: ListSecurityProfilesForTarget
                description: >-
                  <p>Lists the Device Defender security profiles attached to a
                  target (thing group).</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListSecurityProfilesForTarget</a>
                  action.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - For
                  - Target
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
            /streams:
              GET:
                summary: ListStreams
                description: >-
                  <p>Lists all of the streams in your Amazon Web Services
                  account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListStreams</a>
                  action.</p>
                tags:
                  - Lists
                  - Streams
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
            /tags:
              POST:
                summary: TagResource
                description: >-
                  <p>Adds to or modifies the tags of the given resource. Tags
                  are metadata which can be used to manage a resource.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TagResource</a>
                  action.</p>
                tags:
                  - Tags
                  - Resources
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /policy-targets/{policyName}:
              POST:
                summary: ListTargetsForPolicy
                description: >-
                  <p>List targets for the specified policy.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListTargetsForPolicy</a>
                  action.</p>
                tags:
                  - Lists
                  - Targets
                  - For
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /thing-groups:
              GET:
                summary: ListThingGroups
                description: >-
                  <p>List the thing groups in your account.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingGroups</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Groups
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /things/{thingName}/thing-groups:
              GET:
                summary: ListThingGroupsForThing
                description: >-
                  <p>List the thing groups to which the specified thing
                  belongs.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingGroupsForThing</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Groups
                  - For
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /thing-registration-tasks/{taskId}/reports:
              GET:
                summary: ListThingRegistrationTaskReports
                description: <p>Information about the thing registration tasks.</p>
                tags:
                  - Lists
                  - Things
                  - Registrations
                  - Tasks
                  - Reports
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
            /thing-registration-tasks:
              POST:
                summary: StartThingRegistrationTask
                description: >-
                  <p>Creates a bulk thing provisioning task.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartThingRegistrationTask</a>
                  action.</p>
                tags:
                  - Start
                  - Things
                  - Registrations
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
            /thing-types:
              GET:
                summary: ListThingTypes
                description: >-
                  <p>Lists the existing thing types.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingTypes</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Types
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /things:
              POST:
                summary: RegisterThing
                description: >-
                  <p>Provisions a thing in the device registry. RegisterThing
                  calls other IoT control plane APIs. These calls might exceed
                  your account level <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html#limits_iot">
                  IoT Throttling Limits</a> and cause throttle errors. Please
                  contact <a
                  href="https://console.aws.amazon.com/support/home">Amazon Web
                  Services Customer Support</a> to raise your throttling limits
                  if necessary.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RegisterThing</a>
                  action.</p>
                tags:
                  - Register
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /billing-groups/{billingGroupName}/things:
              GET:
                summary: ListThingsInBillingGroup
                description: >-
                  <p>Lists the things you have added to the given billing
                  group.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingsInBillingGroup</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - In
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /thing-groups/{thingGroupName}/things:
              GET:
                summary: ListThingsInThingGroup
                description: >-
                  <p>Lists the things in the specified group.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingsInThingGroup</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - In
                  - Things
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /rules:
              GET:
                summary: ListTopicRules
                description: >-
                  <p>Lists the rules for the specific topic.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListTopicRules</a>
                  action.</p>
                tags:
                  - Lists
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
            /violation-events:
              GET:
                summary: ListViolationEvents
                description: >-
                  <p>Lists the Device Defender security profile violations
                  discovered during the given time period. You can use filters
                  to limit the results to those alerts issued for a particular
                  security profile, behavior, or thing (device).</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListViolationEvents</a>
                  action.</p>
                tags:
                  - Lists
                  - Violations
                  - Events
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
            /violations/verification-state/{violationId}:
              POST:
                summary: PutVerificationStateOnViolation
                description: >-
                  <p>Set a verification state and provide a description of that
                  verification state on a violation (detect alarm).</p>
                tags:
                  - Put
                  - Verification
                  - States
                  - 'On'
                  - Violations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
            /cacertificate:
              POST:
                summary: RegisterCACertificate
                description: >-
                  <p>Registers a CA certificate with Amazon Web Services IoT
                  Core. There is no limit to the number of CA certificates you
                  can register in your Amazon Web Services account. You can
                  register up to 10 CA certificates with the same <code>CA
                  subject field</code> per Amazon Web Services account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RegisterCACertificate</a>
                  action.</p>
                tags:
                  - Register
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
            /certificate/register:
              POST:
                summary: RegisterCertificate
                description: >-
                  <p>Registers a device certificate with IoT in the same <a
                  href="https://docs.aws.amazon.com/iot/latest/apireference/API_CertificateDescription.html#iot-Type-CertificateDescription-certificateMode">certificate
                  mode</a> as the signing CA. If you have more than one CA
                  certificate that has the same subject field, you must specify
                  the CA certificate that was used to sign the device
                  certificate being registered.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RegisterCertificate</a>
                  action.</p>
                tags:
                  - Register
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
            /certificate/register-no-ca:
              POST:
                summary: RegisterCertificateWithoutCA
                description: >-
                  <p>Register a certificate that does not have a certificate
                  authority (CA). For supported certificates, consult <a
                  href="https://docs.aws.amazon.com/iot/latest/developerguide/x509-client-certs.html#x509-cert-algorithms">
                  Certificate signing algorithms supported by IoT</a>. </p>
                tags:
                  - Register
                  - Certificates
                  - Without
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
            /reject-certificate-transfer/{certificateId}:
              PATCH:
                summary: RejectCertificateTransfer
                description: >-
                  <p>Rejects a pending certificate transfer. After IoT rejects a
                  certificate transfer, the certificate status changes from
                  <b>PENDING_TRANSFER</b> to <b>INACTIVE</b>.</p> <p>To check
                  for pending certificate transfers, call
                  <a>ListCertificates</a> to enumerate your certificates.</p>
                  <p>This operation can only be called by the transfer
                  destination. After it is called, the certificate will be
                  returned to the source's account in the INACTIVE state.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RejectCertificateTransfer</a>
                  action.</p>
                tags:
                  - Reject
                  - Certificates
                  - Transfers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
            /billing-groups/removeThingFromBillingGroup:
              PUT:
                summary: RemoveThingFromBillingGroup
                description: >-
                  <p>Removes the given thing from the billing group.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RemoveThingFromBillingGroup</a>
                  action.</p> <note> <p>This call is asynchronous. It might take
                  several seconds for the detachment to propagate.</p> </note>
                tags:
                  - Removes
                  - Things
                  - From
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
            /thing-groups/removeThingFromThingGroup:
              PUT:
                summary: RemoveThingFromThingGroup
                description: >-
                  <p>Remove the specified thing from the specified group.</p>
                  <p>You must specify either a <code>thingGroupArn</code> or a
                  <code>thingGroupName</code> to identify the thing group and
                  either a <code>thingArn</code> or a <code>thingName</code> to
                  identify the thing to remove from the thing group. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RemoveThingFromThingGroup</a>
                  action.</p>
                tags:
                  - Removes
                  - Things
                  - From
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
            /indices/search:
              POST:
                summary: SearchIndex
                description: >-
                  <p>The query search index.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SearchIndex</a>
                  action.</p>
                tags:
                  - Search
                  - Index
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
            /thing-registration-tasks/{taskId}/cancel:
              PUT:
                summary: StopThingRegistrationTask
                description: >-
                  <p>Cancels a bulk thing provisioning task.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StopThingRegistrationTask</a>
                  action.</p>
                tags:
                  - Stop
                  - Things
                  - Registrations
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
            /test-authorization:
              POST:
                summary: TestAuthorization
                description: >-
                  <p>Tests if a specified principal is authorized to perform an
                  IoT action on a specified resource. Use this to test and debug
                  the authorization behavior of devices that connect to the IoT
                  device gateway.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TestAuthorization</a>
                  action.</p>
                tags:
                  - Tests
                  - Authorization
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
            /authorizer/{authorizerName}/test:
              POST:
                summary: TestInvokeAuthorizer
                description: >-
                  <p>Tests a custom authorization behavior by invoking a
                  specified custom authorizer. Use this to test and debug the
                  custom authorization behavior of devices that connect to the
                  IoT device gateway.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TestInvokeAuthorizer</a>
                  action.</p>
                tags:
                  - Tests
                  - Invoke
                  - Authorizer
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
            /transfer-certificate/{certificateId}:
              PATCH:
                summary: TransferCertificate
                description: >-
                  <p>Transfers the specified certificate to the specified Amazon
                  Web Services account.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TransferCertificate</a>
                  action.</p> <p>You can cancel the transfer until it is
                  acknowledged by the recipient.</p> <p>No notification is sent
                  to the transfer destination's account. It is up to the caller
                  to notify the transfer target.</p> <p>The certificate being
                  transferred must not be in the ACTIVE state. You can use the
                  <a>UpdateCertificate</a> action to deactivate it.</p> <p>The
                  certificate must not have any policies attached to it. You can
                  use the <a>DetachPolicy</a> action to detach them.</p>
                tags:
                  - Transfers
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
            /untag:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes the given tags (metadata) from the resource.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UntagResource</a>
                  action.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
            /audit/suppressions/update:
              PATCH:
                summary: UpdateAuditSuppression
                description: <p> Updates a Device Defender audit suppression. </p>
                tags:
                  - Update
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
            /thing-groups/updateThingGroupsForThing:
              PUT:
                summary: UpdateThingGroupsForThing
                description: >-
                  <p>Updates the groups to which the thing belongs.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateThingGroupsForThing</a>
                  action.</p>
                tags:
                  - Update
                  - Things
                  - Groups
                  - For
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
            /security-profile-behaviors/validate:
              POST:
                summary: ValidateSecurityProfileBehaviors
                description: >-
                  <p>Validates a Device Defender security profile behaviors
                  specification.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ValidateSecurityProfileBehaviors</a>
                  a
                tags:
                  - Validate
                  - Security
                  - Profiles
                  - Behaviors
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
                  - Behaviors
                  - Validate
    overlays:
      - type: APIs.io Search
        url: overlays/iot-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot
  - name: oam
    description: >-
      <p>Use Amazon CloudWatch Observability Access Manager to create and manage
      links between source accounts and monitoring accounts by using
      <i>CloudWatch cross-account observability</i>. With CloudWatch
      cross-account observability, you can monitor and troubleshoot applications
      that span multiple accounts within a Region. Seamlessly search, visualize,
      and analyze your metrics, logs, traces, and Application Insights
      applications in any of the linked accounts without account boundaries.</p>
      <p>Set up one or more Amazon Web Services accounts as <i>monitoring
      accounts</i> and link them with multiple <i>source accounts</i>. A
      monitoring account is a central Amazon Web Services account that can view
      and interact with observability data generated from source accounts. A
      source account is an individual Amazon Web Services account that generates
      observability data for the resources that reside in it. Source accounts
      share their observability data with the monitoring account. The shared
      observability data can include metrics in Amazon CloudWatch, logs in
      Amazon CloudWatch Logs, traces in X-Ray, and applications in Amazon
      CloudWatch Application Insights.</p>
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
            title: oam
          paths:
            /CreateLink:
              POST:
                summary: CreateLink
                description: >-
                  <p>Creates a link between a source account and a sink that you
                  have created in a monitoring account.</p> <p>Before you create
                  a link, you must create a sink in the monitoring account and
                  create a sink policy in that account. The sink policy must
                  permit the source account to link to it. You can grant
                  permission to source accounts by granting permission to an
                  entire organization or to individual accounts.</p> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_CreateSink.html">CreateSink</a>
                  and <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_PutSinkPolicy.html">PutSinkPolicy</a>.</p>
                  <p>Each monitoring account can be linked to as many as 100,000
                  source accounts.</p> <p>Each source account can be linked to
                  as many as five monitoring accounts.</p>
                tags:
                  - Create
                  - Link
                  - Create
                  - Link
            /CreateSink:
              POST:
                summary: CreateSink
                description: >-
                  <p>Use this to create a <i>sink</i> in the current account, so
                  that it can be used as a monitoring account in CloudWatch
                  cross-account observability. A sink is a resource that
                  represents an attachment point in a monitoring account. Source
                  accounts can link to the sink to send observability data.</p>
                  <p>After you create a sink, you must create a sink policy that
                  allows source accounts to attach to it. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_PutSinkPolicy.html">PutSinkPolicy</a>.</p>
                  <p>Each account can contain one sink. If you delete a sink,
                  you can then create a new one in that account.</p>
                tags:
                  - Create
                  - Sink
                  - Create
                  - Link
                  - Sink
            /DeleteLink:
              POST:
                summary: DeleteLink
                description: >-
                  <p>Deletes a link between a monitoring account sink and a
                  source account. You must run this operation in the source
                  account.</p>
                tags:
                  - Delete
                  - Link
                  - Create
                  - Link
                  - Sink
                  - Delete
            /DeleteSink:
              POST:
                summary: DeleteSink
                description: >-
                  <p>Deletes a sink. You must delete all links to a sink before
                  you can delete that sink.</p>
                tags:
                  - Delete
                  - Sink
                  - Create
                  - Link
                  - Sink
                  - Delete
            /GetLink:
              POST:
                summary: GetLink
                description: >-
                  <p>Returns complete information about one link.</p> <p>To use
                  this operation, provide the link ARN. To retrieve a list of
                  link ARNs, use <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_ListLinks.html">ListLinks</a>.</p>
                tags:
                  - Get
                  - Link
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
            /GetSink:
              POST:
                summary: GetSink
                description: >-
                  <p>Returns complete information about one monitoring account
                  sink.</p> <p>To use this operation, provide the sink ARN. To
                  retrieve a list of sink ARNs, use <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_ListSinks.html">ListSinks</a>.</p>
                tags:
                  - Get
                  - Sink
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
            /GetSinkPolicy:
              POST:
                summary: GetSinkPolicy
                description: >-
                  <p>Returns the current sink policy attached to this sink. The
                  sink policy specifies what accounts can attach to this sink as
                  source accounts, and what types of data they can share.</p>
                tags:
                  - Get
                  - Sink
                  - Policies
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
            /ListAttachedLinks:
              POST:
                summary: ListAttachedLinks
                description: >-
                  <p>Returns a list of source account links that are linked to
                  this monitoring account sink.</p> <p>To use this operation,
                  provide the sink ARN. To retrieve a list of sink ARNs, use <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_ListSinks.html">ListSinks</a>.</p>
                  <p>To find a list of links for one source account, use <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_ListLinks.html">ListLinks</a>.</p>
                tags:
                  - Lists
                  - Attached
                  - Links
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
                  - Lists
                  - Attached
                  - Links
            /ListLinks:
              POST:
                summary: ListLinks
                description: >-
                  <p>Use this operation in a source account to return a list of
                  links to monitoring account sinks that this source account
                  has.</p> <p>To find a list of links for one monitoring account
                  sink, use <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_ListAttachedLinks.html">ListAttachedLinks</a>
                  from within the monitoring account.</p>
                tags:
                  - Lists
                  - Links
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
                  - Lists
                  - Attached
                  - Links
            /ListSinks:
              POST:
                summary: ListSinks
                description: >-
                  <p>Use this operation in a monitoring account to return the
                  list of sinks created in that account.</p>
                tags:
                  - Lists
                  - Sinks
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
                  - Lists
                  - Attached
                  - Links
                  - Sinks
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from the specified resource.</p>
                  <important> <p>Unlike tagging permissions in other Amazon Web
                  Services services, to tag or untag links and sinks you must
                  have the <code>oam:ResourceTag</code> permission. The
                  <code>iam:TagResource</code> permission does not allow you to
                  tag and untag links and sinks.</p> </important>
                tags:
                  - Untag
                  - Resources
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
                  - Lists
                  - Attached
                  - Links
                  - Sinks
                  - Resources
                  - ARN
            /PutSinkPolicy:
              POST:
                summary: PutSinkPolicy
                description: >-
                  <p>Creates or updates the resource policy that grants
                  permissions to source accounts to link to the monitoring
                  account sink. When you create a sink policy, you can grant
                  permissions to all accounts in an organization or to
                  individual accounts.</p> <p>You can also use a sink policy to
                  limit the types of data that is shared. The three types that
                  you can allow or deny are:</p> <ul> <li> <p> <b>Metrics</b> -
                  Specify with <code>AWS::CloudWatch::Metric</code> </p> </li>
                  <li> <p> <b>Log groups</b> - Specify with
                  <code>AWS::Logs::LogGroup</code> </p> </li> <li> <p>
                  <b>Traces</b> - Specify with <code>AWS::XRay::Trace</code>
                  </p> </li> <li> <p> <b>Application Insights - Applications</b>
                  - Specify with
                  <code>AWS::ApplicationInsights::Application</code> </p> </li>
                  </ul> <p>See the examples in this section to see how to
                  specify permitted source accounts and data types.</p>
                tags:
                  - Put
                  - Sink
                  - Policies
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
                  - Lists
                  - Attached
                  - Links
                  - Sinks
                  - Resources
                  - ARN
                  - Put
            /UpdateLink:
              POST:
                summary: UpdateLink
                description: >-
                  <p>Use this operation to change what types of data are shared
                  from a source account to its linked monitoring account sink.
                  You can't change the sink or change the monitoring account
                  with this operation.</p> <p>To update the list of tags
                  associated with the sink, use <a
                  href="https://docs.aws.amazon.com/OAM/latest/APIReference/API_TagResource.html">TagResourc
                tags:
                  - Update
                  - Link
                  - Create
                  - Link
                  - Sink
                  - Delete
                  - Get
                  - Policies
                  - Lists
                  - Attached
                  - Links
                  - Sinks
                  - Resources
                  - ARN
                  - Put
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/oam-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/oam-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:oam
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---