---
name: Activation
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/activation.png
url: https://example.com/apis/activation.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Activation
apis:
  - name: omics
    description: >-
      <p>This is the <i>AWS HealthOmics API Reference</i>. For an introduction
      to the service, see <a
      href="https://docs.aws.amazon.com/omics/latest/dev/">What is AWS
      HealthOmics?</a> in the <i>AWS HealthOmics User Guide</i>.</p>
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
            title: omics
          paths:
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/abort:
              DELETE:
                summary: AbortMultipartReadSetUpload
                description: <p> Stops a multipart upload. </p>
                tags:
                  - Abort
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
            /share/{shareId}:
              GET:
                summary: GetShare
                description: <p> Retrieves the metadata for a share. </p>
                tags:
                  - Get
                  - Share
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
            /sequencestore/{sequenceStoreId}/readset/batch/delete:
              POST:
                summary: BatchDeleteReadSet
                description: <p>Deletes one or more read sets.</p>
                tags:
                  - Batches
                  - Delete
                  - Read
                  - Sets
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
            /import/annotation/{jobId}:
              GET:
                summary: GetAnnotationImportJob
                description: <p>Gets information about an annotation import job.</p>
                tags:
                  - Get
                  - Annotations
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
            /run/{id}/cancel:
              POST:
                summary: CancelRun
                description: <p>Cancels a run.</p>
                tags:
                  - Cancel
                  - Runs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
            /import/variant/{jobId}:
              GET:
                summary: GetVariantImportJob
                description: <p>Gets information about a variant import job.</p>
                tags:
                  - Get
                  - Variants
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/complete:
              POST:
                summary: CompleteMultipartReadSetUpload
                description: >-
                  <p> Concludes a multipart upload once you have uploaded all
                  the components. </p>
                tags:
                  - Complete
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
            /annotationStore:
              POST:
                summary: CreateAnnotationStore
                description: <p>Creates an annotation store.</p>
                tags:
                  - Create
                  - Annotations
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
            /annotationStore/{name}/version:
              POST:
                summary: CreateAnnotationStoreVersion
                description: <p> Creates a new version of an annotation store. </p>
                tags:
                  - Create
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
            /sequencestore/{sequenceStoreId}/upload:
              POST:
                summary: CreateMultipartReadSetUpload
                description: <p> Begins a multipart read set upload. </p>
                tags:
                  - Create
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
            /referencestore:
              POST:
                summary: CreateReferenceStore
                description: <p>Creates a reference store.</p>
                tags:
                  - Create
                  - References
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
            /runGroup:
              GET:
                summary: ListRunGroups
                description: <p>Retrieves a list of run groups.</p>
                tags:
                  - Lists
                  - Runs
                  - Groups
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
            /sequencestore:
              POST:
                summary: CreateSequenceStore
                description: <p>Creates a sequence store.</p>
                tags:
                  - Create
                  - Sequence
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
            /share:
              POST:
                summary: CreateShare
                description: >-
                  <p> Creates a share offer that can be accepted outside the
                  account by a subscriber. The share is created by the owner and
                  accepted by the principal subscriber. </p>
                tags:
                  - Create
                  - Share
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
            /variantStore:
              POST:
                summary: CreateVariantStore
                description: <p>Creates a variant store.</p>
                tags:
                  - Create
                  - Variants
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
            /workflow:
              GET:
                summary: ListWorkflows
                description: <p>Retrieves a list of workflows.</p>
                tags:
                  - Lists
                  - Workflows
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
            /annotationStore/{name}:
              POST:
                summary: UpdateAnnotationStore
                description: <p>Updates an annotation store.</p>
                tags:
                  - Update
                  - Annotations
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
            /annotationStore/{name}/versions/delete:
              POST:
                summary: DeleteAnnotationStoreVersions
                description: >-
                  <p> Deletes one or multiple versions of an annotation store.
                  </p>
                tags:
                  - Delete
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
            /referencestore/{referenceStoreId}/reference/{id}:
              GET:
                summary: GetReference
                description: <p>Gets a reference file.</p>
                tags:
                  - Get
                  - References
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /referencestore/{id}:
              GET:
                summary: GetReferenceStore
                description: <p>Gets information about a reference store.</p>
                tags:
                  - Get
                  - References
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /run/{id}:
              GET:
                summary: GetRun
                description: <p>Gets information about a workflow run.</p>
                tags:
                  - Get
                  - Runs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /runGroup/{id}:
              POST:
                summary: UpdateRunGroup
                description: <p>Updates a run group.</p>
                tags:
                  - Update
                  - Runs
                  - Group
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /sequencestore/{id}:
              GET:
                summary: GetSequenceStore
                description: <p>Gets information about a sequence store.</p>
                tags:
                  - Get
                  - Sequence
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /variantStore/{name}:
              POST:
                summary: UpdateVariantStore
                description: <p>Updates a variant store.</p>
                tags:
                  - Update
                  - Variants
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /workflow/{id}:
              POST:
                summary: UpdateWorkflow
                description: <p>Updates a workflow.</p>
                tags:
                  - Update
                  - Workflows
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /annotationStore/{name}/version/{versionName}:
              POST:
                summary: UpdateAnnotationStoreVersion
                description: >-
                  <p> Updates the description of an annotation store version.
                  </p>
                tags:
                  - Update
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /sequencestore/{sequenceStoreId}/readset/{id}:
              GET:
                summary: GetReadSet
                description: <p>Gets a file from a read set.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /sequencestore/{sequenceStoreId}/activationjob/{id}:
              GET:
                summary: GetReadSetActivationJob
                description: <p>Gets information about a read set activation job.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Activation
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
            /sequencestore/{sequenceStoreId}/exportjob/{id}:
              GET:
                summary: GetReadSetExportJob
                description: <p>Gets information about a read set export job.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Export
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
            /sequencestore/{sequenceStoreId}/importjob/{id}:
              GET:
                summary: GetReadSetImportJob
                description: <p>Gets information about a read set import job.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
            /sequencestore/{sequenceStoreId}/readset/{id}/metadata:
              GET:
                summary: GetReadSetMetadata
                description: <p>Gets details about a read set.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Metadata
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /referencestore/{referenceStoreId}/importjob/{id}:
              GET:
                summary: GetReferenceImportJob
                description: <p>Gets information about a reference import job.</p>
                tags:
                  - Get
                  - References
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /referencestore/{referenceStoreId}/reference/{id}/metadata:
              GET:
                summary: GetReferenceMetadata
                description: <p>Gets information about a genome reference's metadata.</p>
                tags:
                  - Get
                  - References
                  - Metadata
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /run/{id}/task/{taskId}:
              GET:
                summary: GetRunTask
                description: <p>Gets information about a workflow run task.</p>
                tags:
                  - Get
                  - Runs
                  - Tasks
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /import/annotations:
              POST:
                summary: ListAnnotationImportJobs
                description: <p>Retrieves a list of annotation import jobs.</p>
                tags:
                  - Lists
                  - Annotations
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
            /annotationStore/{name}/versions:
              POST:
                summary: ListAnnotationStoreVersions
                description: <p> Lists the versions of an annotation store. </p>
                tags:
                  - Lists
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
            /annotationStores:
              POST:
                summary: ListAnnotationStores
                description: <p>Retrieves a list of annotation stores.</p>
                tags:
                  - Lists
                  - Annotations
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
            /sequencestore/{sequenceStoreId}/uploads:
              POST:
                summary: ListMultipartReadSetUploads
                description: >-
                  <p> Lists multipart read set uploads and for in progress
                  uploads. Once the upload is completed, a read set is created
                  and the upload will no longer be returned in the respone. </p>
                tags:
                  - Lists
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
            /sequencestore/{sequenceStoreId}/activationjobs:
              POST:
                summary: ListReadSetActivationJobs
                description: <p>Retrieves a list of read set activation jobs.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Activation
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
            /sequencestore/{sequenceStoreId}/exportjobs:
              POST:
                summary: ListReadSetExportJobs
                description: <p>Retrieves a list of read set export jobs.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Export
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
            /sequencestore/{sequenceStoreId}/importjobs:
              POST:
                summary: ListReadSetImportJobs
                description: <p>Retrieves a list of read set import jobs.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/parts:
              POST:
                summary: ListReadSetUploadParts
                description: >-
                  <p> This operation will list all parts in a requested
                  multipart upload for a sequence store. </p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Uploads
                  - Parts
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
            /sequencestore/{sequenceStoreId}/readsets:
              POST:
                summary: ListReadSets
                description: <p>Retrieves a list of read sets.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
            /referencestore/{referenceStoreId}/importjobs:
              POST:
                summary: ListReferenceImportJobs
                description: <p>Retrieves a list of reference import jobs.</p>
                tags:
                  - Lists
                  - References
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
            /referencestores:
              POST:
                summary: ListReferenceStores
                description: <p>Retrieves a list of reference stores.</p>
                tags:
                  - Lists
                  - References
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
            /referencestore/{referenceStoreId}/references:
              POST:
                summary: ListReferences
                description: <p>Retrieves a list of references.</p>
                tags:
                  - Lists
                  - References
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
            /run/{id}/task:
              GET:
                summary: ListRunTasks
                description: <p>Retrieves a list of tasks for a run.</p>
                tags:
                  - Lists
                  - Runs
                  - Tasks
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
            /run:
              POST:
                summary: StartRun
                description: >-
                  <p>Starts a workflow run. To duplicate a run, specify the
                  run's ID and a role ARN. The remaining parameters are copied
                  from the previous run.</p> <p>The total number of runs in your
                  account is subject to a quota per Region. To avoid needing to
                  delete runs manually, you can set the retention mode to
                  <code>REMOVE</code>. Runs with this setting are deleted
                  automatically when the run quoata is exceeded.</p>
                tags:
                  - Start
                  - Runs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
            /sequencestores:
              POST:
                summary: ListSequenceStores
                description: <p>Retrieves a list of sequence stores.</p>
                tags:
                  - Lists
                  - Sequence
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
            /shares:
              POST:
                summary: ListShares
                description: <p> Lists all shares associated with an account. </p>
                tags:
                  - Lists
                  - Shares
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
            /import/variants:
              POST:
                summary: ListVariantImportJobs
                description: <p>Retrieves a list of variant import jobs.</p>
                tags:
                  - Lists
                  - Variants
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
            /variantStores:
              POST:
                summary: ListVariantStores
                description: <p>Retrieves a list of variant stores.</p>
                tags:
                  - Lists
                  - Variants
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
            /import/annotation:
              POST:
                summary: StartAnnotationImportJob
                description: <p>Starts an annotation import job.</p>
                tags:
                  - Start
                  - Annotations
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /sequencestore/{sequenceStoreId}/activationjob:
              POST:
                summary: StartReadSetActivationJob
                description: >-
                  <p>Activates an archived read set. To reduce storage charges,
                  Amazon Omics archives unused read sets after 30 days.</p>
                tags:
                  - Start
                  - Read
                  - Sets
                  - Activation
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /sequencestore/{sequenceStoreId}/exportjob:
              POST:
                summary: StartReadSetExportJob
                description: <p>Exports a read set to Amazon S3.</p>
                tags:
                  - Start
                  - Read
                  - Sets
                  - Export
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /sequencestore/{sequenceStoreId}/importjob:
              POST:
                summary: StartReadSetImportJob
                description: <p>Starts a read set import job.</p>
                tags:
                  - Start
                  - Read
                  - Sets
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /referencestore/{referenceStoreId}/importjob:
              POST:
                summary: StartReferenceImportJob
                description: <p>Starts a reference import job.</p>
                tags:
                  - Start
                  - References
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /import/variant:
              POST:
                summary: StartVariantImportJob
                description: <p>Starts a variant import job.</p>
                tags:
                  - Start
                  - Variants
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
                  - Variants
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/part:
              PUT:
                summary: UploadReadSetPart
                description: >-
                  <p> This operation uploads a specific part of a read set. If
                  you upload a new part using a previously used part number, the
                  previously uploaded part will be overwri
                tags:
                  - Uploads
                  - Read
                  - Sets
                  - Part
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
                  - Variants
                  - Pa
    overlays:
      - type: APIs.io Search
        url: overlays/omics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/omics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:omics
  - name: workdocs
    description: >-
      <p>The Amazon WorkDocs API is designed for the following use cases:</p>
      <ul> <li> <p>File Migration: File migration applications are supported for
      users who want to migrate their files from an on-premises or off-premises
      file system or service. Users can insert files into a user directory
      structure, as well as allow for basic metadata changes, such as
      modifications to the permissions of files.</p> </li> <li> <p>Security:
      Support security applications are supported for users who have additional
      security needs, such as antivirus or data loss prevention. The API
      actions, along with CloudTrail, allow these applications to detect when
      changes occur in Amazon WorkDocs. Then, the application can take the
      necessary actions and replace the target file. If the target file violates
      the policy, the application can also choose to email the user.</p> </li>
      <li> <p>eDiscovery/Analytics: General administrative applications are
      supported, such as eDiscovery and analytics. These applications can choose
      to mimic or record the actions in an Amazon WorkDocs site, along with
      CloudTrail, to replicate data for eDiscovery, backup, or analytical
      applications.</p> </li> </ul> <p>All Amazon WorkDocs API actions are
      Amazon authenticated and certificate-signed. They not only require the use
      of the Amazon Web Services SDK, but also allow for the exclusive use of
      IAM users and roles to help facilitate access, trust, and permission
      policies. By creating a role and allowing an IAM user to access the Amazon
      WorkDocs site, the IAM user gains full administrative visibility into the
      entire Amazon WorkDocs site (or as set in the IAM policy). This includes,
      but is not limited to, the ability to modify file permissions and upload
      any file to any user. This allows developers to perform the three use
      cases above, as well as give users the ability to grant access on a
      selective basis using the IAM model.</p> <note> <p>The pricing for Amazon
      WorkDocs APIs varies depending on the API call type for these actions:</p>
      <ul> <li> <p> <code>READ (Get*)</code> </p> </li> <li> <p> <code>WRITE
      (Activate*, Add*, Create*, Deactivate*, Initiate*, Update*)</code> </p>
      </li> <li> <p> <code>LIST (Describe*)</code> </p> </li> <li> <p>
      <code>DELETE*, CANCEL</code> </p> </li> </ul> <p>For information about
      Amazon WorkDocs API pricing, see <a
      href="https://aws.amazon.com/workdocs/pricing/">Amazon WorkDocs
      Pricing</a>.</p> </note>
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
            title: workdocs
          paths:
            /api/v1/documents/{DocumentId}/versions/{VersionId}:
              PATCH:
                summary: UpdateDocumentVersion
                description: >-
                  <p>Changes the status of the document version to ACTIVE. </p>
                  <p>Amazon WorkDocs also sets its document container to ACTIVE.
                  This is the last step in a document upload, after the client
                  uploads the document to an S3-presigned URL returned by
                  <a>InitiateDocumentVersionUpload</a>. </p>
                tags:
                  - Update
                  - Document
                  - Versions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
            /api/v1/users/{UserId}/activation:
              DELETE:
                summary: DeactivateUser
                description: >-
                  <p>Deactivates the specified user, which revokes the user's
                  access to Amazon WorkDocs.</p>
                tags:
                  - Deactivate
                  - Users
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
            /api/v1/resources/{ResourceId}/permissions:
              DELETE:
                summary: RemoveAllResourcePermissions
                description: >-
                  <p>Removes all the permissions from the specified
                  resource.</p>
                tags:
                  - Removes
                  - All
                  - Resources
                  - Permissions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
            /api/v1/documents/{DocumentId}/versions/{VersionId}/comment:
              POST:
                summary: CreateComment
                description: <p>Adds a new comment to the specified document version.</p>
                tags:
                  - Create
                  - Comments
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
            /api/v1/resources/{ResourceId}/customMetadata:
              DELETE:
                summary: DeleteCustomMetadata
                description: <p>Deletes custom metadata from the specified resource.</p>
                tags:
                  - Delete
                  - Custom
                  - Metadata
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
            /api/v1/folders:
              POST:
                summary: CreateFolder
                description: >-
                  <p>Creates a folder with the specified name and parent
                  folder.</p>
                tags:
                  - Create
                  - Folder
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
            /api/v1/resources/{ResourceId}/labels:
              DELETE:
                summary: DeleteLabels
                description: <p>Deletes the specified list of labels from a resource.</p>
                tags:
                  - Delete
                  - Labels
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
            /api/v1/organizations/{OrganizationId}/subscriptions:
              GET:
                summary: DescribeNotificationSubscriptions
                description: <p>Lists the specified notification subscriptions.</p>
                tags:
                  - Describe
                  - Notifications
                  - Subscriptions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
            /api/v1/users:
              GET:
                summary: DescribeUsers
                description: >-
                  <p>Describes the specified users. You can describe all users
                  or filter the results (for example, by status or
                  organization).</p> <p>By default, Amazon WorkDocs returns the
                  first 24 active or pending users. If there are more results,
                  the response includes a marker that you can use to request the
                  next set of results.</p>
                tags:
                  - Describe
                  - Users
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
            /api/v1/documents/{DocumentId}/versions/{VersionId}/comment/{CommentId}:
              DELETE:
                summary: DeleteComment
                description: >-
                  <p>Deletes the specified comment from the document
                  version.</p>
                tags:
                  - Delete
                  - Comments
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
            /api/v1/documents/{DocumentId}:
              PATCH:
                summary: UpdateDocument
                description: >-
                  <p>Updates the specified attributes of a document. The user
                  must have access to both the document and its parent folder,
                  if applicable.</p>
                tags:
                  - Update
                  - Document
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
            /api/v1/documentVersions/{DocumentId}/versions/{VersionId}:
              DELETE:
                summary: DeleteDocumentVersion
                description: <p>Deletes a specific version of a document.</p>
                tags:
                  - Delete
                  - Document
                  - Versions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
            /api/v1/folders/{FolderId}:
              PATCH:
                summary: UpdateFolder
                description: >-
                  <p>Updates the specified attributes of the specified folder.
                  The user must have access to both the folder and its parent
                  folder, if applicable.</p>
                tags:
                  - Update
                  - Folder
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
            /api/v1/folders/{FolderId}/contents:
              GET:
                summary: DescribeFolderContents
                description: >-
                  <p>Describes the contents of the specified folder, including
                  its documents and subfolders.</p> <p>By default, Amazon
                  WorkDocs returns the first 100 active document and folder
                  metadata items. If there are more results, the response
                  includes a marker that you can use to request the next set of
                  results. You can also request initialized documents.</p>
                tags:
                  - Describe
                  - Folder
                  - Contents
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
            /api/v1/organizations/{OrganizationId}/subscriptions/{SubscriptionId}:
              DELETE:
                summary: DeleteNotificationSubscription
                description: >-
                  <p>Deletes the specified subscription from the specified
                  organization.</p>
                tags:
                  - Delete
                  - Notifications
                  - Subscriptions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
            /api/v1/users/{UserId}:
              PATCH:
                summary: UpdateUser
                description: >-
                  <p>Updates the specified attributes of the specified user, and
                  grants or revokes administrative privileges to the Amazon
                  WorkDocs site.</p>
                tags:
                  - Update
                  - Users
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
            /api/v1/activities:
              GET:
                summary: DescribeActivities
                description: >-
                  <p>Describes the user activities in a specified time
                  period.</p>
                tags:
                  - Describe
                  - Activities
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
            /api/v1/documents/{DocumentId}/versions/{VersionId}/comments:
              GET:
                summary: DescribeComments
                description: >-
                  <p>List all the comments for the specified document
                  version.</p>
                tags:
                  - Describe
                  - Comments
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
            /api/v1/documents/{DocumentId}/versions:
              GET:
                summary: DescribeDocumentVersions
                description: >-
                  <p>Retrieves the document versions for the specified
                  document.</p> <p>By default, only active versions are
                  returned.</p>
                tags:
                  - Describe
                  - Document
                  - Versions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
            /api/v1/groups:
              GET:
                summary: DescribeGroups
                description: >-
                  <p>Describes the groups specified by the query. Groups are
                  defined by the underlying Active Directory.</p>
                tags:
                  - Describe
                  - Groups
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
            /api/v1/me/root:
              GET:
                summary: DescribeRootFolders
                description: >-
                  <p>Describes the current user's special folders; the
                  <code>RootFolder</code> and the <code>RecycleBin</code>.
                  <code>RootFolder</code> is the root of user's files and
                  folders and <code>RecycleBin</code> is the root of recycled
                  items. This is not a valid action for SigV4 (administrative
                  API) clients.</p> <p>This action requires an authentication
                  token. To get an authentication token, register an application
                  with Amazon WorkDocs. For more information, see <a
                  href="https://docs.aws.amazon.com/workdocs/latest/developerguide/wd-auth-user.html">Authentication
                  and Access Control for User Applications</a> in the <i>Amazon
                  WorkDocs Developer Guide</i>.</p>
                tags:
                  - Describe
                  - Root
                  - Folders
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
            /api/v1/me:
              GET:
                summary: GetCurrentUser
                description: >-
                  <p>Retrieves details of the current user for whom the
                  authentication token was generated. This is not a valid action
                  for SigV4 (administrative API) clients.</p> <p>This action
                  requires an authentication token. To get an authentication
                  token, register an application with Amazon WorkDocs. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/workdocs/latest/developerguide/wd-auth-user.html">Authentication
                  and Access Control for User Applications</a> in the <i>Amazon
                  WorkDocs Developer Guide</i>.</p>
                tags:
                  - Get
                  - Current
                  - Users
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
            /api/v1/documents/{DocumentId}/path:
              GET:
                summary: GetDocumentPath
                description: >-
                  <p>Retrieves the path information (the hierarchy from the root
                  folder) for the requested document.</p> <p>By default, Amazon
                  WorkDocs returns a maximum of 100 levels upwards from the
                  requested document and only includes the IDs of the parent
                  folders in the path. You can limit the maximum number of
                  levels. You can also request the names of the parent
                  folders.</p>
                tags:
                  - Get
                  - Document
                  - Paths
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
            /api/v1/folders/{FolderId}/path:
              GET:
                summary: GetFolderPath
                description: >-
                  <p>Retrieves the path information (the hierarchy from the root
                  folder) for the specified folder.</p> <p>By default, Amazon
                  WorkDocs returns a maximum of 100 levels upwards from the
                  requested folder and only includes the IDs of the parent
                  folders in the path. You can limit the maximum number of
                  levels. You can also request the parent folder names.</p>
                tags:
                  - Get
                  - Folder
                  - Paths
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
            /api/v1/resources:
              GET:
                summary: GetResources
                description: >-
                  <p>Retrieves a collection of resources, including folders and
                  documents. The only <code>CollectionType</code> supported is
                  <code>SHARED_WITH_ME</code>.</p>
                tags:
                  - Get
                  - Resources
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
                  - Resources
            /api/v1/documents:
              POST:
                summary: InitiateDocumentVersionUpload
                description: >-
                  <p>Creates a new document object and version object.</p>
                  <p>The client specifies the parent folder ID and name of the
                  document to upload. The ID is optionally specified when
                  creating a new version of an existing document. This is the
                  first step to upload a document. Next, upload the document to
                  the URL returned from the call, and then call
                  <a>UpdateDocumentVersion</a>.</p> <p>To cancel the document
                  upload, call <a>AbortDocumentVersionUpload</a>.</p>
                tags:
                  - Initiate
                  - Document
                  - Versions
                  - Uploads
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
                  - Resources
                  - Documents
            /api/v1/resources/{ResourceId}/permissions/{PrincipalId}:
              DELETE:
                summary: RemoveResourcePermission
                description: >-
                  <p>Removes the permission for the specified principal from the
                  specified resource.</p>
                tags:
                  - Removes
                  - Resources
                  - Permission
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
                  - Resources
                  - Documents
                  - Principals
            /api/v1/documentVersions/restore/{DocumentId}:
              POST:
                summary: RestoreDocumentVersions
                description: >-
                  <p>Recovers a deleted version of an Amazon WorkDocs
                  document.</p>
                tags:
                  - Restore
                  - Document
                  - Versions
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
                  - Resources
                  - Documents
                  - Principals
                  - Restore
            /api/v1/search:
              POST:
                summary: SearchResources
                description: >-
                  <p>Searches metadata and the content of folders, documents,
                  document versions, and com
                tags:
                  - Search
                  - Resources
                  - Document
                  - Identifiers
                  - Versions
                  - Versions
                  - Users
                  - Activation
                  - Resources
                  - Permissions
                  - Comments
                  - Custom
                  - Metadata
                  - APIs
                  - V1
                  - Folders
                  - Labels
                  - Organizations
                  - Subscriptions
                  - Users
                  - Folder
                  - Contents
                  - Subscriptions
                  - Activities
                  - Comments
                  - Groups
                  - Me
                  - Root
                  - Paths
                  - Resources
                  - Documents
                  - Principals
                  - Restore
                  - Search
    overlays:
      - type: APIs.io Search
        url: overlays/workdocs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workdocs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workdocs
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---