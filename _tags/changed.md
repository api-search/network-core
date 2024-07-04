---
name: Changed
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/changed.png
url: https://example.com/apis/changed.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Changed
apis:
  - name: ebs
    description: >-
      <p>You can use the Amazon Elastic Block Store (Amazon EBS) direct APIs to
      create Amazon EBS snapshots, write data directly to your snapshots, read
      data on your snapshots, and identify the differences or changes between
      two snapshots. If you’re an independent software vendor (ISV) who offers
      backup services for Amazon EBS, the EBS direct APIs make it more efficient
      and cost-effective to track incremental changes on your Amazon EBS volumes
      through snapshots. This can be done without having to create new volumes
      from snapshots, and then use Amazon Elastic Compute Cloud (Amazon EC2)
      instances to compare the differences.</p> <p>You can create incremental
      snapshots directly from data on-premises into volumes and the cloud to use
      for quick disaster recovery. With the ability to write and read snapshots,
      you can write your on-premises data to an snapshot during a disaster. Then
      after recovery, you can restore it back to Amazon Web Services or
      on-premises from the snapshot. You no longer need to build and maintain
      complex mechanisms to copy data to and from Amazon EBS.</p> <p>This API
      reference provides detailed information about the actions, data types,
      parameters, and errors of the EBS direct APIs. For more information about
      the elements that make up the EBS direct APIs, and examples of how to use
      them effectively, see <a
      href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-accessing-snapshot.html">Accessing
      the Contents of an Amazon EBS Snapshot</a> in the <i>Amazon Elastic
      Compute Cloud User Guide</i>. For more information about the supported
      Amazon Web Services Regions, endpoints, and service quotas for the EBS
      direct APIs, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/ebs-service.html">Amazon
      Elastic Block Store Endpoints and Quotas</a> in the <i>Amazon Web Services
      General Reference</i>.</p>
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
            title: ebs
          paths:
            /snapshots/completion/{snapshotId}:
              POST:
                summary: CompleteSnapshot
                description: >-
                  <p>Seals and completes the snapshot after all of the required
                  blocks of data have been written to it. Completing the
                  snapshot changes the status to <code>completed</code>. You
                  cannot write new blocks to a snapshot after it has been
                  completed.</p> <note> <p>You should always retry requests that
                  receive server (<code>5xx</code>) error responses, and
                  <code>ThrottlingException</code> and
                  <code>RequestThrottledException</code> client error responses.
                  For more information see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/error-retries.html">Error
                  retries</a> in the <i>Amazon Elastic Compute Cloud User
                  Guide</i>.</p> </note>
                tags:
                  - Complete
                  - Snapshots
                  - Identifiers
            /snapshots/{snapshotId}/blocks/{blockIndex}:
              PUT:
                summary: PutSnapshotBlock
                description: >-
                  <p>Writes a block of data to a snapshot. If the specified
                  block contains data, the existing data is overwritten. The
                  target snapshot must be in the <code>pending</code> state.</p>
                  <p>Data written to a snapshot must be aligned with 512-KiB
                  sectors.</p> <note> <p>You should always retry requests that
                  receive server (<code>5xx</code>) error responses, and
                  <code>ThrottlingException</code> and
                  <code>RequestThrottledException</code> client error responses.
                  For more information see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/error-retries.html">Error
                  retries</a> in the <i>Amazon Elastic Compute Cloud User
                  Guide</i>.</p> </note>
                tags:
                  - Put
                  - Snapshots
                  - Blocks
                  - Identifiers
                  - Blocks
                  - Blocks
                  - Index
            /snapshots/{secondSnapshotId}/changedblocks:
              GET:
                summary: ListChangedBlocks
                description: >-
                  <p>Returns information about the blocks that are different
                  between two Amazon Elastic Block Store snapshots of the same
                  volume/snapshot lineage.</p> <note> <p>You should always retry
                  requests that receive server (<code>5xx</code>) error
                  responses, and <code>ThrottlingException</code> and
                  <code>RequestThrottledException</code> client error responses.
                  For more information see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/error-retries.html">Error
                  retries</a> in the <i>Amazon Elastic Compute Cloud User
                  Guide</i>.</p> </note>
                tags:
                  - Lists
                  - Changed
                  - Blocks
                  - Identifiers
                  - Blocks
                  - Blocks
                  - Index
                  - Snapshots
                  - Changed Blocks
            /snapshots/{snapshotId}/blocks:
              GET:
                summary: ListSnapshotBlocks
                description: >-
                  <p>Returns information about the blocks in an Amazon Elastic
                  Block Store snapshot.</p> <note> <p>You should always retry
                  requests that receive server (<code>5xx</code>) error
                  responses, and <code>ThrottlingException</code> and
                  <code>RequestThrottledException</code> client error responses.
                  For more information see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/error-retries.html">Error
                  retries</a> in the <i>Amazon Elastic Compute Cloud User
                  Guide</i>.</p> </note>
                tags:
                  - Lists
                  - Snapshots
                  - Blocks
                  - Identifiers
                  - Blocks
                  - Blocks
                  - Index
                  - Snapshots
                  - Changed Blocks
            /snapshots:
              POST:
                summary: StartSnapshot
                description: >-
                  <p>Creates a new Amazon EBS snapshot. The new snapshot enters
                  the <code>pending</code> state after the request completes.
                  </p> <p>After creating the snapshot, use <a
                  href="https://docs.aws.amazon.com/ebs/latest/APIReference/API_PutSnapshotBlock.html">
                  PutSnapshotBlock</a> to write blocks of data to the
                  snapshot.</p> <note> <p>You should always retry requests that
                  receive server (<code>5xx</code>) error responses, and
                  <code>ThrottlingException</code> and
                  <code>RequestThrottledException</code> client error responses.
                  For more information see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/error-retries.html">Error
                  retries</a> in the <i>Amazon Elastic Compute Cloud User
                  Guide</i>.</
                tags:
                  - Start
                  - Snapshots
                  - Identifiers
                  - Blocks
                  - Blocks
                  - Index
                  - Snapshots
                  - Changed Blocks
                  - Snapshots
    overlays:
      - type: APIs.io Search
        url: overlays/ebs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ebs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ebs
  - aid: box:box-shield-information-barriers-api
    name: Box Shield Information Barriers API
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
            title: Box Shield Information Barriers API
          paths:
            /shield_information_barriers/{shield_information_barrier_id}:
              get:
                summary: Get shield information barrier with specified ID
                tags:
                  - Get
                  - Shield
                  - Information
                  - Barrier
                  - With
                  - Specified
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                description: Get shield information barrier based on provided ID.
            /shield_information_barriers/change_status:
              post:
                summary: >-
                  Add changed status of shield information barrier with
                  specified ID
                tags:
                  - Add
                  - Changed
                  - Status
                  - Of
                  - Shield
                  - Information
                  - Barrier
                  - With
                  - Specified
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                  - Change_status
                description: >-
                  Change status of shield information barrier with the specified
                  ID.
            /shield_information_barriers:
              get:
                summary: List shield information barriers
                tags:
                  - List
                  - Shield
                  - Information
                  - Barriers
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                  - Change_status
                description: |-
                  Retrieves a list of shield information barrier objects
                  for the enterprise of JWT.
              post:
                summary: Create shield information barrier
                tags:
                  - Create
                  - Shield
                  - Information
                  - Barrier
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                  - Change_status
                description: |-
                  Creates a shield information barrier to
                  separate individuals/groups within the same
                  firm and prevents confidential information passing b
    overlays:
      - type: APIs.io Search
        url: overlays/shield-information-barriers-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/shield-information-barriers-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---