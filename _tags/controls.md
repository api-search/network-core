---
name: Controls
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/controls.png
url: https://example.com/apis/controls.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Controls
apis:
  - name: auditmanager
    description: >-
      <p>Welcome to the Audit Manager API reference. This guide is for
      developers who need detailed information about the Audit Manager API
      operations, data types, and errors. </p> <p>Audit Manager is a service
      that provides automated evidence collection so that you can continually
      audit your Amazon Web Services usage. You can use it to assess the
      effectiveness of your controls, manage risk, and simplify compliance.</p>
      <p>Audit Manager provides prebuilt frameworks that structure and automate
      assessments for a given compliance standard. Frameworks include a prebuilt
      collection of controls with descriptions and testing procedures. These
      controls are grouped according to the requirements of the specified
      compliance standard or regulation. You can also customize frameworks and
      controls to support internal audits with specific requirements. </p>
      <p>Use the following links to get started with the Audit Manager API:</p>
      <ul> <li> <p> <a
      href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Operations.html">Actions</a>:
      An alphabetical list of all Audit Manager API operations.</p> </li> <li>
      <p> <a
      href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Types.html">Data
      types</a>: An alphabetical list of all Audit Manager data types.</p> </li>
      <li> <p> <a
      href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/CommonParameters.html">Common
      parameters</a>: Parameters that all operations can use.</p> </li> <li> <p>
      <a
      href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/CommonErrors.html">Common
      errors</a>: Client and server errors that all operations can return.</p>
      </li> </ul> <p>If you're new to Audit Manager, we recommend that you
      review the <a
      href="https://docs.aws.amazon.com/audit-manager/latest/userguide/what-is.html">
      Audit Manager User Guide</a>.</p>
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
            title: auditmanager
          paths:
            /assessments/{assessmentId}/associateToAssessmentReport:
              PUT:
                summary: AssociateAssessmentReportEvidenceFolder
                description: >-
                  <p> Associates an evidence folder to an assessment report in
                  an Audit Manager assessment. </p>
                tags:
                  - Associate
                  - Assessments
                  - Reports
                  - Evidence
                  - Folder
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
            /assessments/{assessmentId}/batchAssociateToAssessmentReport:
              PUT:
                summary: BatchAssociateAssessmentReportEvidence
                description: >-
                  <p> Associates a list of evidence to an assessment report in
                  an Audit Manager assessment. </p>
                tags:
                  - Batches
                  - Associate
                  - Assessments
                  - Reports
                  - Evidence
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
            /assessments/{assessmentId}/delegations:
              PUT:
                summary: BatchDeleteDelegationByAssessment
                description: >-
                  <p> Deletes a batch of delegations for an assessment in Audit
                  Manager. </p>
                tags:
                  - Batches
                  - Delete
                  - Delegation
                  - By
                  - Assessments
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
            /assessments/{assessmentId}/batchDisassociateFromAssessmentReport:
              PUT:
                summary: BatchDisassociateAssessmentReportEvidence
                description: >-
                  <p> Disassociates a list of evidence from an assessment report
                  in Audit Manager. </p>
                tags:
                  - Batches
                  - Disassociate
                  - Assessments
                  - Reports
                  - Evidence
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
            /assessments/{assessmentId}/controlSets/{controlSetId}/controls/{controlId}/evidence:
              POST:
                summary: BatchImportEvidenceToAssessmentControl
                description: >-
                  <p>Adds one or more pieces of evidence to a control in an
                  Audit Manager assessment. </p> <p>You can import manual
                  evidence from any S3 bucket by specifying the S3 URI of the
                  object. You can also upload a file from your browser, or enter
                  plain text in response to a risk assessment question. </p>
                  <p>The following restrictions apply to this action:</p> <ul>
                  <li> <p> <code>manualEvidence</code> can be only one of the
                  following: <code>evidenceFileName</code>,
                  <code>s3ResourcePath</code>, or <code>textResponse</code> </p>
                  </li> <li> <p>Maximum size of an individual evidence file: 100
                  MB</p> </li> <li> <p>Number of daily manual evidence uploads
                  per control: 100</p> </li> <li> <p>Supported file formats: See
                  <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/upload-evidence.html#supported-manual-evidence-files">Supported
                  file types for manual evidence</a> in the <i>Audit Manager
                  User Guide</i> </p> </li> </ul> <p>For more information about
                  Audit Manager service restrictions, see <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/service-quotas.html">Quotas
                  and restrictions for Audit Manager</a>.</p>
                tags:
                  - Batches
                  - Import
                  - Evidence
                  - To
                  - Assessments
                  - Control
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
            /assessments:
              GET:
                summary: ListAssessments
                description: >-
                  <p> Returns a list of current and past assessments from Audit
                  Manager. </p>
                tags:
                  - Lists
                  - Assessments
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
            /assessmentFrameworks:
              GET:
                summary: ListAssessmentFrameworks
                description: >-
                  <p> Returns a list of the frameworks that are available in the
                  Audit Manager framework library. </p>
                tags:
                  - Lists
                  - Assessments
                  - Frameworks
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
            /assessments/{assessmentId}/reports:
              POST:
                summary: CreateAssessmentReport
                description: >-
                  <p> Creates an assessment report for the specified assessment.
                  </p>
                tags:
                  - Create
                  - Assessments
                  - Reports
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
            /controls:
              GET:
                summary: ListControls
                description: <p> Returns a list of controls from Audit Manager. </p>
                tags:
                  - Lists
                  - Controls
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
            /assessments/{assessmentId}:
              PUT:
                summary: UpdateAssessment
                description: <p> Edits an Audit Manager assessment. </p>
                tags:
                  - Update
                  - Assessments
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
            /assessmentFrameworks/{frameworkId}:
              PUT:
                summary: UpdateAssessmentFramework
                description: <p> Updates a custom framework in Audit Manager. </p>
                tags:
                  - Update
                  - Assessments
                  - Frameworks
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
            /assessmentFrameworkShareRequests/{requestId}:
              PUT:
                summary: UpdateAssessmentFrameworkShare
                description: >-
                  <p> Updates a share request for a custom framework in Audit
                  Manager. </p>
                tags:
                  - Update
                  - Assessments
                  - Frameworks
                  - Share
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
            /assessments/{assessmentId}/reports/{assessmentReportId}:
              DELETE:
                summary: DeleteAssessmentReport
                description: >-
                  <p>Deletes an assessment report in Audit Manager. </p> <p>When
                  you run the <code>DeleteAssessmentReport</code> operation,
                  Audit Manager attempts to delete the following data:</p> <ol>
                  <li> <p>The specified assessment report that’s stored in your
                  S3 bucket</p> </li> <li> <p>The associated metadata that’s
                  stored in Audit Manager</p> </li> </ol> <p>If Audit Manager
                  can’t access the assessment report in your S3 bucket, the
                  report isn’t deleted. In this event, the
                  <code>DeleteAssessmentReport</code> operation doesn’t fail.
                  Instead, it proceeds to delete the associated metadata only.
                  You must then delete the assessment report from the S3 bucket
                  yourself. </p> <p>This scenario happens when Audit Manager
                  receives a <code>403 (Forbidden)</code> or <code>404 (Not
                  Found)</code> error from Amazon S3. To avoid this, make sure
                  that your S3 bucket is available, and that you configured the
                  correct permissions for Audit Manager to delete resources in
                  your S3 bucket. For an example permissions policy that you can
                  use, see <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/security_iam_id-based-policy-examples.html#full-administrator-access-assessment-report-destination">Assessment
                  report destination permissions</a> in the <i>Audit Manager
                  User Guide</i>. For information about the issues that could
                  cause a <code>403 (Forbidden)</code> or <code>404 (Not
                  Found</code>) error from Amazon S3, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#ErrorCodeList">List
                  of Error Codes</a> in the <i>Amazon Simple Storage Service API
                  Reference</i>. </p>
                tags:
                  - Delete
                  - Assessments
                  - Reports
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
            /controls/{controlId}:
              PUT:
                summary: UpdateControl
                description: <p> Updates a custom control in Audit Manager. </p>
                tags:
                  - Update
                  - Control
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
            /account/deregisterAccount:
              POST:
                summary: DeregisterAccount
                description: >-
                  <p> Deregisters an account in Audit Manager. </p> <note>
                  <p>Before you deregister, you can use the <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_UpdateSettings.html">UpdateSettings</a>
                  API operation to set your preferred data retention policy. By
                  default, Audit Manager retains your data. If you want to
                  delete your data, you can use the
                  <code>DeregistrationPolicy</code> attribute to request the
                  deletion of your data. </p> <p>For more information about data
                  retention, see <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/data-protection.html">Data
                  Protection</a> in the <i>Audit Manager User Guide</i>. </p>
                  </note>
                tags:
                  - Deregister
                  - Account
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
            /account/deregisterOrganizationAdminAccount:
              POST:
                summary: DeregisterOrganizationAdminAccount
                description: >-
                  <p>Removes the specified Amazon Web Services account as a
                  delegated administrator for Audit Manager. </p> <p>When you
                  remove a delegated administrator from your Audit Manager
                  settings, you continue to have access to the evidence that you
                  previously collected under that account. This is also the case
                  when you deregister a delegated administrator from
                  Organizations. However, Audit Manager stops collecting and
                  attaching evidence to that delegated administrator account
                  moving forward.</p> <important> <p>Keep in mind the following
                  cleanup task if you use evidence finder:</p> <p>Before you use
                  your management account to remove a delegated administrator,
                  make sure that the current delegated administrator account
                  signs in to Audit Manager and disables evidence finder first.
                  Disabling evidence finder automatically deletes the event data
                  store that was created in their account when they enabled
                  evidence finder. If this task isn’t completed, the event data
                  store remains in their account. In this case, we recommend
                  that the original delegated administrator goes to CloudTrail
                  Lake and manually <a
                  href="https://docs.aws.amazon.com/awscloudtrail/latest/userguide/query-eds-disable-termination.html">deletes
                  the event data store</a>.</p> <p>This cleanup task is
                  necessary to ensure that you don't end up with multiple event
                  data stores. Audit Manager ignores an unused event data store
                  after you remove or change a delegated administrator account.
                  However, the unused event data store continues to incur
                  storage costs from CloudTrail Lake if you don't delete it.</p>
                  </important> <p>When you deregister a delegated administrator
                  account for Audit Manager, the data for that account isn’t
                  deleted. If you want to delete resource data for a delegated
                  administrator account, you must perform that task separately
                  before you deregister the account. Either, you can do this in
                  the Audit Manager console. Or, you can use one of the delete
                  API operations that are provided by Audit Manager. </p> <p>To
                  delete your Audit Manager resource data, see the following
                  instructions: </p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteAssessment.html">DeleteAssessment</a>
                  (see also: <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/delete-assessment.html">Deleting
                  an assessment</a> in the <i>Audit Manager User Guide</i>)</p>
                  </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteAssessmentFramework.html">DeleteAssessmentFramework</a>
                  (see also: <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/delete-custom-framework.html">Deleting
                  a custom framework</a> in the <i>Audit Manager User
                  Guide</i>)</p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteAssessmentFrameworkShare.html">DeleteAssessmentFrameworkShare</a>
                  (see also: <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/deleting-shared-framework-requests.html">Deleting
                  a share request</a> in the <i>Audit Manager User
                  Guide</i>)</p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteAssessmentReport.html">DeleteAssessmentReport</a>
                  (see also: <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/generate-assessment-report.html#delete-assessment-report-steps">Deleting
                  an assessment report</a> in the <i>Audit Manager User
                  Guide</i>)</p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteControl.html">DeleteControl</a>
                  (see also: <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/delete-controls.html">Deleting
                  a custom control</a> in the <i>Audit Manager User
                  Guide</i>)</p> </li> </ul> <p>At this time, Audit Manager
                  doesn't provide an option to delete evidence for a specific
                  delegated administrator. Instead, when your management account
                  deregisters Audit Manager, we perform a cleanup for the
                  current delegated administrator account at the time of
                  deregistration.</p>
                tags:
                  - Deregister
                  - Organizations
                  - Administrative
                  - Account
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
            /assessments/{assessmentId}/disassociateFromAssessmentReport:
              PUT:
                summary: DisassociateAssessmentReportEvidenceFolder
                description: >-
                  <p> Disassociates an evidence folder from the specified
                  assessment report in Audit Manager. </p>
                tags:
                  - Disassociate
                  - Assessments
                  - Reports
                  - Evidence
                  - Folder
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
            /account/status:
              GET:
                summary: GetAccountStatus
                description: >-
                  <p> Gets the registration status of an account in Audit
                  Manager. </p>
                tags:
                  - Get
                  - Account
                  - Status
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
            /assessments/{assessmentId}/reports/{assessmentReportId}/url:
              GET:
                summary: GetAssessmentReportUrl
                description: >-
                  <p> Gets the URL of an assessment report in Audit Manager.
                  </p>
                tags:
                  - Get
                  - Assessments
                  - Reports
                  - URL
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
            /assessments/{assessmentId}/changelogs:
              GET:
                summary: GetChangeLogs
                description: <p> Gets a list of changelogs from Audit Manager. </p>
                tags:
                  - Get
                  - Change
                  - Logs
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
            /delegations:
              GET:
                summary: GetDelegations
                description: >-
                  <p> Gets a list of delegations from an audit owner to a
                  delegate. </p>
                tags:
                  - Get
                  - Delegations
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
            /assessments/{assessmentId}/controlSets/{controlSetId}/evidenceFolders/{evidenceFolderId}/evidence/{evidenceId}:
              GET:
                summary: GetEvidence
                description: <p> Gets information about a specified evidence item.</p>
                tags:
                  - Get
                  - Evidence
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
            /assessments/{assessmentId}/controlSets/{controlSetId}/evidenceFolders/{evidenceFolderId}/evidence:
              GET:
                summary: GetEvidenceByEvidenceFolder
                description: >-
                  <p> Gets all evidence from a specified evidence folder in
                  Audit Manager. </p>
                tags:
                  - Get
                  - Evidence
                  - By
                  - Folder
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
            /evidenceFileUploadUrl:
              GET:
                summary: GetEvidenceFileUploadUrl
                description: >-
                  <p>Creates a presigned Amazon S3 URL that can be used to
                  upload a file as manual evidence. For instructions on how to
                  use this operation, see <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/upload-evidence.html#how-to-upload-manual-evidence-files">Upload
                  a file from your browser </a> in the <i>Audit Manager User
                  Guide</i>.</p> <p>The following restrictions apply to this
                  operation:</p> <ul> <li> <p>Maximum size of an individual
                  evidence file: 100 MB</p> </li> <li> <p>Number of daily manual
                  evidence uploads per control: 100</p> </li> <li> <p>Supported
                  file formats: See <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/upload-evidence.html#supported-manual-evidence-files">Supported
                  file types for manual evidence</a> in the <i>Audit Manager
                  User Guide</i> </p> </li> </ul> <p>For more information about
                  Audit Manager service restrictions, see <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/service-quotas.html">Quotas
                  and restrictions for Audit Manager</a>.</p>
                tags:
                  - Get
                  - Evidence
                  - File
                  - Uploads
                  - URL
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
            /assessments/{assessmentId}/controlSets/{controlSetId}/evidenceFolders/{evidenceFolderId}:
              GET:
                summary: GetEvidenceFolder
                description: >-
                  <p> Gets an evidence folder from a specified assessment in
                  Audit Manager. </p>
                tags:
                  - Get
                  - Evidence
                  - Folder
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
            /assessments/{assessmentId}/evidenceFolders:
              GET:
                summary: GetEvidenceFoldersByAssessment
                description: >-
                  <p> Gets the evidence folders from a specified assessment in
                  Audit Manager. </p>
                tags:
                  - Get
                  - Evidence
                  - Folders
                  - By
                  - Assessments
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
            /assessments/{assessmentId}/evidenceFolders-by-assessment-control/{controlSetId}/{controlId}:
              GET:
                summary: GetEvidenceFoldersByAssessmentControl
                description: >-
                  <p> Gets a list of evidence folders that are associated with a
                  specified control in an Audit Manager assessment. </p>
                tags:
                  - Get
                  - Evidence
                  - Folders
                  - By
                  - Assessments
                  - Control
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
            /insights:
              GET:
                summary: GetInsights
                description: >-
                  <p>Gets the latest analytics data for all your current active
                  assessments. </p>
                tags:
                  - Get
                  - Insights
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
            /insights/assessments/{assessmentId}:
              GET:
                summary: GetInsightsByAssessment
                description: >-
                  <p>Gets the latest analytics data for a specific active
                  assessment. </p>
                tags:
                  - Get
                  - Insights
                  - By
                  - Assessments
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
            /account/organizationAdminAccount:
              GET:
                summary: GetOrganizationAdminAccount
                description: >-
                  <p> Gets the name of the delegated Amazon Web Services
                  administrator account for a specified organization. </p>
                tags:
                  - Get
                  - Organizations
                  - Administrative
                  - Account
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
            /services:
              GET:
                summary: GetServicesInScope
                description: >-
                  <p>Gets a list of all of the Amazon Web Services that you can
                  choose to include in your assessment. When you <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_CreateAssessment.html">create
                  an assessment</a>, specify which of these services you want to
                  include to narrow the assessment's <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Scope.html">scope</a>.</p>
                tags:
                  - Get
                  - Services
                  - In
                  - Scopes
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
            /settings/{attribute}:
              GET:
                summary: GetSettings
                description: >-
                  <p> Gets the settings for a specified Amazon Web Services
                  account. </p>
                tags:
                  - Get
                  - Settings
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
            /insights/controls-by-assessment:
              GET:
                summary: ListAssessmentControlInsightsByControlDomain
                description: >-
                  <p>Lists the latest analytics data for controls within a
                  specific control domain and a specific active assessment.</p>
                  <note> <p>Control insights are listed only if the control
                  belongs to the control domain and assessment that was
                  specified. Moreover, the control must have collected evidence
                  on the <code>lastUpdated</code> date of
                  <code>controlInsightsByAssessment</code>. If neither of these
                  conditions are met, no data is listed for that control. </p>
                  </note>
                tags:
                  - Lists
                  - Assessments
                  - Control
                  - Insights
                  - By
                  - Domains
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
            /assessmentFrameworkShareRequests:
              GET:
                summary: ListAssessmentFrameworkShareRequests
                description: >-
                  <p> Returns a list of sent or received share requests for
                  custom frameworks in Audit Manager. </p>
                tags:
                  - Lists
                  - Assessments
                  - Frameworks
                  - Share
                  - null
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
            /assessmentReports:
              GET:
                summary: ListAssessmentReports
                description: >-
                  <p> Returns a list of assessment reports created in Audit
                  Manager. </p>
                tags:
                  - Lists
                  - Assessments
                  - Reports
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
            /insights/control-domains:
              GET:
                summary: ListControlDomainInsights
                description: >-
                  <p>Lists the latest analytics data for control domains across
                  all of your active assessments. </p> <note> <p>A control
                  domain is listed only if at least one of the controls within
                  that domain collected evidence on the <code>lastUpdated</code>
                  date of <code>controlDomainInsights</code>. If this condition
                  isn’t met, no data is listed for that control domain.</p>
                  </note>
                tags:
                  - Lists
                  - Control
                  - Domains
                  - Insights
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
            /insights/control-domains-by-assessment:
              GET:
                summary: ListControlDomainInsightsByAssessment
                description: >-
                  <p>Lists analytics data for control domains within a specified
                  active assessment.</p> <note> <p>A control domain is listed
                  only if at least one of the controls within that domain
                  collected evidence on the <code>lastUpdated</code> date of
                  <code>controlDomainInsights</code>. If this condition isn’t
                  met, no data is listed for that domain.</p> </note>
                tags:
                  - Lists
                  - Control
                  - Domains
                  - Insights
                  - By
                  - Assessments
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
            /insights/controls:
              GET:
                summary: ListControlInsightsByControlDomain
                description: >-
                  <p>Lists the latest analytics data for controls within a
                  specific control domain across all active assessments.</p>
                  <note> <p>Control insights are listed only if the control
                  belongs to the control domain that was specified and the
                  control collected evidence on the <code>lastUpdated</code>
                  date of <code>controlInsightsMetadata</code>. If neither of
                  these conditions are met, no data is listed for that control.
                  </p> </note>
                tags:
                  - Lists
                  - Control
                  - Insights
                  - By
                  - Domains
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
            /dataSourceKeywords:
              GET:
                summary: ListKeywordsForDataSource
                description: >-
                  <p> Returns a list of keywords that are pre-mapped to the
                  specified control data source. </p>
                tags:
                  - Lists
                  - Keywords
                  - For
                  - Data
                  - Source
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
            /notifications:
              GET:
                summary: ListNotifications
                description: <p> Returns a list of all Audit Manager notifications. </p>
                tags:
                  - Lists
                  - Notifications
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p> Removes a tag from a resource in Audit Manager. </p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /account/registerAccount:
              POST:
                summary: RegisterAccount
                description: >-
                  <p> Enables Audit Manager for the specified Amazon Web
                  Services account. </p>
                tags:
                  - Register
                  - Account
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /account/registerOrganizationAdminAccount:
              POST:
                summary: RegisterOrganizationAdminAccount
                description: >-
                  <p> Enables an Amazon Web Services account within the
                  organization as the delegated administrator for Audit Manager.
                  </p>
                tags:
                  - Register
                  - Organizations
                  - Administrative
                  - Account
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /assessmentFrameworks/{frameworkId}/shareRequests:
              POST:
                summary: StartAssessmentFrameworkShare
                description: >-
                  <p> Creates a share request for a custom framework in Audit
                  Manager. </p> <p>The share request specifies a recipient and
                  notifies them that a custom framework is available. Recipients
                  have 120 days to accept or decline the request. If no action
                  is taken, the share request expires.</p> <p>When you create a
                  share request, Audit Manager stores a snapshot of your custom
                  framework in the US East (N. Virginia) Amazon Web Services
                  Region. Audit Manager also stores a backup of the same
                  snapshot in the US West (Oregon) Amazon Web Services
                  Region.</p> <p>Audit Manager deletes the snapshot and the
                  backup snapshot when one of the following events occurs:</p>
                  <ul> <li> <p>The sender revokes the share request.</p> </li>
                  <li> <p>The recipient declines the share request.</p> </li>
                  <li> <p>The recipient encounters an error and doesn't
                  successfully accept the share request.</p> </li> <li> <p>The
                  share request expires before the recipient responds to the
                  request.</p> </li> </ul> <p>When a sender <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/framework-sharing.html#framework-sharing-resend">resends
                  a share request</a>, the snapshot is replaced with an updated
                  version that corresponds with the latest version of the custom
                  framework. </p> <p>When a recipient accepts a share request,
                  the snapshot is replicated into their Amazon Web Services
                  account under the Amazon Web Services Region that was
                  specified in the share request. </p> <important> <p>When you
                  invoke the <code>StartAssessmentFrameworkShare</code> API, you
                  are about to share a custom framework with another Amazon Web
                  Services account. You may not share a custom framework that is
                  derived from a standard framework if the standard framework is
                  designated as not eligible for sharing by Amazon Web Services,
                  unless you have obtained permission to do so from the owner of
                  the standard framework. To learn more about which standard
                  frameworks are eligible for sharing, see <a
                  href="https://docs.aws.amazon.com/audit-manager/latest/userguide/share-custom-framework-concepts-and-terminology.html#eligibility">Framework
                  sharing eligibility</a> in the <i>Audit Manager User
                  Guide</i>.</p> </important>
                tags:
                  - Start
                  - Assessments
                  - Frameworks
                  - Share
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /assessments/{assessmentId}/controlSets/{controlSetId}/controls/{controlId}:
              PUT:
                summary: UpdateAssessmentControl
                description: >-
                  <p> Updates a control within an assessment in Audit Manager.
                  </p>
                tags:
                  - Update
                  - Assessments
                  - Control
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /assessments/{assessmentId}/controlSets/{controlSetId}/status:
              PUT:
                summary: UpdateAssessmentControlSetStatus
                description: >-
                  <p> Updates the status of a control set in an Audit Manager
                  assessment. </p>
                tags:
                  - Update
                  - Assessments
                  - Control
                  - Sets
                  - Status
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /assessments/{assessmentId}/status:
              PUT:
                summary: UpdateAssessmentStatus
                description: <p> Updates the status of an assessment in Audit Manager. </p>
                tags:
                  - Update
                  - Assessments
                  - Status
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /settings:
              PUT:
                summary: UpdateSettings
                description: >-
                  <p> Updates Audit Manager settings for the current account.
                  </p>
                tags:
                  - Update
                  - Settings
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
            /assessmentReports/integrity:
              POST:
                summary: ValidateAssessmentReportIntegrity
                description: >-
                  <p> Validates the integrity of an assessment report in Audit
                  Ma
                tags:
                  - Validate
                  - Assessments
                  - Reports
                  - Integrity
                  - Identifiers
                  - Associate
                  - To
                  - Assessments
                  - Reports
                  - Batches
                  - Delegations
                  - Disassociate
                  - From
                  - Control
                  - Sets
                  - Sets
                  - Controls
                  - Evidence
                  - Assessments
                  - Frameworks
                  - Reports
                  - Frameworks
                  - Share
                  - null
                  - Request
                  - Account
                  - Organizations
                  - Administrative
                  - Status
                  - URL
                  - Change Logs
                  - Folders
                  - Folder
                  - File
                  - Uploads
                  - By
                  - Insights
                  - Services
                  - Settings
                  - Attributes
                  - Domains
                  - Source
                  - Keywords
                  - Notifications
                  - ARN
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/auditmanager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/auditmanager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:auditmanager
  - name: cloudfront
    description: >-
      <fullname>Amazon CloudFront</fullname> <p>Amazon CloudFront is a global
      content delivery network (CDN) service that accelerates delivery of your
      websites, APIs, video content or other web assets. It integrates with
      other Amazon Web Services products to give developers and businesses an
      easy way to accelerate content to end users with no minimum usage
      commitments.</p>
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
            title: cloudfront
          paths:
            /2020-05-31/distribution/{TargetDistributionId}/associate-alias:
              PUT:
                summary: AssociateAlias
                description: >-
                  <p>Associates an alias (also known as a CNAME or an alternate
                  domain name) with a CloudFront distribution.</p> <p>With this
                  operation you can move an alias that's already in use on a
                  CloudFront distribution to a different distribution in one
                  step. This prevents the downtime that could occur if you first
                  remove the alias from one distribution and then separately add
                  the alias to another distribution.</p> <p>To use this
                  operation to associate an alias with a distribution, you
                  provide the alias and the ID of the target distribution for
                  the alias. For more information, including how to set up the
                  target distribution, prerequisites that you must complete, and
                  other restrictions, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/CNAMEs.html#alternate-domain-names-move">Moving
                  an alternate domain name to a different distribution</a> in
                  the <i>Amazon CloudFront Developer Guide</i>.</p>
                tags:
                  - Associate
                  - Alias
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
            /2020-05-31/distribution/{PrimaryDistributionId}/copy:
              POST:
                summary: CopyDistribution
                description: >-
                  <p>Creates a staging distribution using the configuration of
                  the provided primary distribution. A staging distribution is a
                  copy of an existing distribution (called the primary
                  distribution) that you can use in a continuous deployment
                  workflow.</p> <p>After you create a staging distribution, you
                  can use <code>UpdateDistribution</code> to modify the staging
                  distribution's configuration. Then you can use
                  <code>CreateContinuousDeploymentPolicy</code> to incrementally
                  move traffic to the staging distribution.</p> <p>This API
                  operation requires the following IAM permissions:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_GetDistribution.html">GetDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html">CreateDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CopyDistribution.html">CopyDistribution</a>
                  </p> </li> </ul>
                tags:
                  - Copy
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
            /2020-05-31/cache-policy:
              GET:
                summary: ListCachePolicies
                description: >-
                  <p>Gets a list of cache policies.</p> <p>You can optionally
                  apply a filter to return only the managed policies created by
                  Amazon Web Services, or only the custom policies created in
                  your Amazon Web Services account.</p> <p>You can optionally
                  specify the maximum number of items to receive in the
                  response. If the total number of items in the list exceeds the
                  maximum that you specify, or the default maximum, the response
                  is paginated. To get the next page of items, send a subsequent
                  request that specifies the <code>NextMarker</code> value from
                  the current response as the <code>Marker</code> value in the
                  subsequent request.</p>
                tags:
                  - Lists
                  - Cache
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
            /2020-05-31/origin-access-identity/cloudfront:
              GET:
                summary: ListCloudFrontOriginAccessIdentities
                description: <p>Lists origin access identities.</p>
                tags:
                  - Lists
                  - Cloud
                  - Front
                  - Origin
                  - Access
                  - Identities
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
            /2020-05-31/continuous-deployment-policy:
              GET:
                summary: ListContinuousDeploymentPolicies
                description: >-
                  <p>Gets a list of the continuous deployment policies in your
                  Amazon Web Services account.</p> <p>You can optionally specify
                  the maximum number of items to receive in the response. If the
                  total number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Continuous
                  - Deployments
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
            /2020-05-31/distribution:
              GET:
                summary: ListDistributions
                description: <p>List CloudFront distributions.</p>
                tags:
                  - Lists
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
            /2020-05-31/distribution?WithTags:
              POST:
                summary: CreateDistributionWithTags
                description: >-
                  <p>Create a new distribution with tags. This API operation
                  requires the following IAM permissions:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html">CreateDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_TagResource.html">TagResource</a>
                  </p> </li> </ul>
                tags:
                  - Create
                  - Distributions
                  - null
                  - Tags
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
            /2020-05-31/field-level-encryption:
              GET:
                summary: ListFieldLevelEncryptionConfigs
                description: >-
                  <p>List all field-level encryption configurations that have
                  been created in CloudFront for this account.</p>
                tags:
                  - Lists
                  - Fields
                  - Levels
                  - Encryption
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
            /2020-05-31/field-level-encryption-profile:
              GET:
                summary: ListFieldLevelEncryptionProfiles
                description: >-
                  <p>Request a list of field-level encryption profiles that have
                  been created in CloudFront for this account.</p>
                tags:
                  - Lists
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
            /2020-05-31/function:
              GET:
                summary: ListFunctions
                description: >-
                  <p>Gets a list of all CloudFront functions in your Amazon Web
                  Services account.</p> <p>You can optionally apply a filter to
                  return only the functions that are in the specified stage,
                  either <code>DEVELOPMENT</code> or <code>LIVE</code>.</p>
                  <p>You can optionally specify the maximum number of items to
                  receive in the response. If the total number of items in the
                  list exceeds the maximum that you specify, or the default
                  maximum, the response is paginated. To get the next page of
                  items, send a subsequent request that specifies the
                  <code>NextMarker</code> value from the current response as the
                  <code>Marker</code> value in the subsequent request.</p>
                tags:
                  - Lists
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
            /2020-05-31/distribution/{DistributionId}/invalidation:
              GET:
                summary: ListInvalidations
                description: <p>Lists invalidation batches.</p>
                tags:
                  - Lists
                  - Invalidations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
            /2020-05-31/key-group:
              GET:
                summary: ListKeyGroups
                description: >-
                  <p>Gets a list of key groups.</p> <p>You can optionally
                  specify the maximum number of items to receive in the
                  response. If the total number of items in the list exceeds the
                  maximum that you specify, or the default maximum, the response
                  is paginated. To get the next page of items, send a subsequent
                  request that specifies the <code>NextMarker</code> value from
                  the current response as the <code>Marker</code> value in the
                  subsequent request.</p>
                tags:
                  - Lists
                  - Keys
                  - Groups
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
            /2020-05-31/key-value-store/:
              POST:
                summary: CreateKeyValueStore
                description: >-
                  <p>Specifies the Key Value Store resource to add to your
                  account. In your account, the Key Value Store names must be
                  unique. You can also import Key Value Store data in JSON
                  format from an S3 bucket by providing a valid
                  <code>ImportSource</code> that you own.</p>
                tags:
                  - Create
                  - Keys
                  - Value
                  - Store
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
            /2020-05-31/distributions/{DistributionId}/monitoring-subscription/:
              GET:
                summary: GetMonitoringSubscription
                description: >-
                  <p>Gets information about whether additional CloudWatch
                  metrics are enabled for the specified CloudFront
                  distribution.</p>
                tags:
                  - Get
                  - Monitoring
                  - Subscriptions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
            /2020-05-31/origin-access-control:
              GET:
                summary: ListOriginAccessControls
                description: >-
                  <p>Gets the list of CloudFront origin access controls in this
                  Amazon Web Services account.</p> <p>You can optionally specify
                  the maximum number of items to receive in the response. If the
                  total number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send another request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the next
                  request.</p>
                tags:
                  - Lists
                  - Origin
                  - Access
                  - Controls
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
            /2020-05-31/origin-request-policy:
              GET:
                summary: ListOriginRequestPolicies
                description: >-
                  <p>Gets a list of origin request policies.</p> <p>You can
                  optionally apply a filter to return only the managed policies
                  created by Amazon Web Services, or only the custom policies
                  created in your Amazon Web Services account.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Origin
                  - Request
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
            /2020-05-31/public-key:
              GET:
                summary: ListPublicKeys
                description: >-
                  <p>List all public keys that have been added to CloudFront for
                  this account.</p>
                tags:
                  - Lists
                  - Public
                  - Keys
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
            /2020-05-31/realtime-log-config:
              GET:
                summary: ListRealtimeLogConfigs
                description: >-
                  <p>Gets a list of real-time log configurations.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
            /2020-05-31/response-headers-policy:
              GET:
                summary: ListResponseHeadersPolicies
                description: >-
                  <p>Gets a list of response headers policies.</p> <p>You can
                  optionally apply a filter to get only the managed policies
                  created by Amazon Web Services, or only the custom policies
                  created in your Amazon Web Services account.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Responses
                  - Headers
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
            /2020-05-31/streaming-distribution:
              GET:
                summary: ListStreamingDistributions
                description: <p>List streaming distributions.</p>
                tags:
                  - Lists
                  - Streaming
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/streaming-distribution?WithTags:
              POST:
                summary: CreateStreamingDistributionWithTags
                description: >-
                  <p>This API is deprecated. Amazon CloudFront is deprecating
                  real-time messaging protocol (RTMP) distributions on December
                  31, 2020. For more information, <a
                  href="http://forums.aws.amazon.com/ann.jspa?annID=7356">read
                  the announcement</a> on the Amazon CloudFront discussion
                  forum.</p>
                tags:
                  - Create
                  - Streaming
                  - Distributions
                  - null
                  - Tags
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/cache-policy/{Id}:
              PUT:
                summary: UpdateCachePolicy
                description: >-
                  <p>Updates a cache policy configuration.</p> <p>When you
                  update a cache policy configuration, all the fields are
                  updated with the values provided in the request. You cannot
                  update some fields independent of others. To update a cache
                  policy configuration:</p> <ol> <li> <p>Use
                  <code>GetCachePolicyConfig</code> to get the current
                  configuration.</p> </li> <li> <p>Locally modify the fields in
                  the cache policy configuration that you want to update.</p>
                  </li> <li> <p>Call <code>UpdateCachePolicy</code> by providing
                  the entire cache policy configuration, including the fields
                  that you modified and those that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Cache
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/origin-access-identity/cloudfront/{Id}:
              GET:
                summary: GetCloudFrontOriginAccessIdentity
                description: <p>Get the information about an origin access identity.</p>
                tags:
                  - Get
                  - Cloud
                  - Front
                  - Origin
                  - Access
                  - Identity
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/continuous-deployment-policy/{Id}:
              PUT:
                summary: UpdateContinuousDeploymentPolicy
                description: >-
                  <p>Updates a continuous deployment policy. You can update a
                  continuous deployment policy to enable or disable it, to
                  change the percentage of traffic that it sends to the staging
                  distribution, or to change the staging distribution that it
                  sends traffic to.</p> <p>When you update a continuous
                  deployment policy configuration, all the fields are updated
                  with the values that are provided in the request. You cannot
                  update some fields independent of others. To update a
                  continuous deployment policy configuration:</p> <ol> <li>
                  <p>Use <code>GetContinuousDeploymentPolicyConfig</code> to get
                  the current configuration.</p> </li> <li> <p>Locally modify
                  the fields in the continuous deployment policy configuration
                  that you want to update.</p> </li> <li> <p>Use
                  <code>UpdateContinuousDeploymentPolicy</code>, providing the
                  entire continuous deployment policy configuration, including
                  the fields that you modified and those that you didn't.</p>
                  </li> </ol>
                tags:
                  - Update
                  - Continuous
                  - Deployments
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/distribution/{Id}:
              GET:
                summary: GetDistribution
                description: <p>Get the information about a distribution.</p>
                tags:
                  - Get
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/field-level-encryption/{Id}:
              GET:
                summary: GetFieldLevelEncryption
                description: >-
                  <p>Get the field-level encryption configuration
                  information.</p>
                tags:
                  - Get
                  - Fields
                  - Levels
                  - Encryption
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/field-level-encryption-profile/{Id}:
              GET:
                summary: GetFieldLevelEncryptionProfile
                description: <p>Get the field-level encryption profile information.</p>
                tags:
                  - Get
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/function/{Name}:
              PUT:
                summary: UpdateFunction
                description: >-
                  <p>Updates a CloudFront function.</p> <p>You can update a
                  function's code or the comment that describes the function.
                  You cannot update a function's name.</p> <p>To update a
                  function, you provide the function's name and version
                  (<code>ETag</code> value) along with the updated function
                  code. To get the name and version, you can use
                  <code>ListFunctions</code> and
                  <code>DescribeFunction</code>.</p>
                tags:
                  - Update
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/key-group/{Id}:
              PUT:
                summary: UpdateKeyGroup
                description: >-
                  <p>Updates a key group.</p> <p>When you update a key group,
                  all the fields are updated with the values provided in the
                  request. You cannot update some fields independent of others.
                  To update a key group:</p> <ol> <li> <p>Get the current key
                  group with <code>GetKeyGroup</code> or
                  <code>GetKeyGroupConfig</code>.</p> </li> <li> <p>Locally
                  modify the fields in the key group that you want to update.
                  For example, add or remove public key IDs.</p> </li> <li>
                  <p>Call <code>UpdateKeyGroup</code> with the entire key group
                  object, including the fields that you modified and those that
                  you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Keys
                  - Group
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/key-value-store/{Name}:
              PUT:
                summary: UpdateKeyValueStore
                description: <p>Specifies the Key Value Store to update.</p>
                tags:
                  - Update
                  - Keys
                  - Value
                  - Store
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/origin-access-control/{Id}:
              GET:
                summary: GetOriginAccessControl
                description: >-
                  <p>Gets a CloudFront origin access control, including its
                  unique identifier.</p>
                tags:
                  - Get
                  - Origin
                  - Access
                  - Control
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/origin-request-policy/{Id}:
              PUT:
                summary: UpdateOriginRequestPolicy
                description: >-
                  <p>Updates an origin request policy configuration.</p> <p>When
                  you update an origin request policy configuration, all the
                  fields are updated with the values provided in the request.
                  You cannot update some fields independent of others. To update
                  an origin request policy configuration:</p> <ol> <li> <p>Use
                  <code>GetOriginRequestPolicyConfig</code> to get the current
                  configuration.</p> </li> <li> <p>Locally modify the fields in
                  the origin request policy configuration that you want to
                  update.</p> </li> <li> <p>Call
                  <code>UpdateOriginRequestPolicy</code> by providing the entire
                  origin request policy configuration, including the fields that
                  you modified and those that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Origin
                  - Request
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/public-key/{Id}:
              GET:
                summary: GetPublicKey
                description: <p>Gets a public key.</p>
                tags:
                  - Get
                  - Public
                  - Keys
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/delete-realtime-log-config/:
              POST:
                summary: DeleteRealtimeLogConfig
                description: >-
                  <p>Deletes a real-time log configuration.</p> <p>You cannot
                  delete a real-time log configuration if it's attached to a
                  cache behavior. First update your distributions to remove the
                  real-time log configuration from all cache behaviors, then
                  delete the real-time log configuration.</p> <p>To delete a
                  real-time log configuration, you can provide the
                  configuration's name or its Amazon Resource Name (ARN). You
                  must provide at least one. If you provide both, CloudFront
                  uses the name to identify the real-time log configuration to
                  delete.</p>
                tags:
                  - Delete
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
            /2020-05-31/response-headers-policy/{Id}:
              PUT:
                summary: UpdateResponseHeadersPolicy
                description: >-
                  <p>Updates a response headers policy.</p> <p>When you update a
                  response headers policy, the entire policy is replaced. You
                  cannot update some policy fields independent of others. To
                  update a response headers policy configuration:</p> <ol> <li>
                  <p>Use <code>GetResponseHeadersPolicyConfig</code> to get the
                  current policy's configuration.</p> </li> <li> <p>Modify the
                  fields in the response headers policy configuration that you
                  want to update.</p> </li> <li> <p>Call
                  <code>UpdateResponseHeadersPolicy</code>, providing the entire
                  response headers policy configuration, including the fields
                  that you modified and those that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Responses
                  - Headers
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
            /2020-05-31/streaming-distribution/{Id}:
              GET:
                summary: GetStreamingDistribution
                description: >-
                  <p>Gets information about a specified RTMP distribution,
                  including the distribution configuration.</p>
                tags:
                  - Get
                  - Streaming
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
            /2020-05-31/function/{Name}/describe:
              GET:
                summary: DescribeFunction
                description: >-
                  <p>Gets configuration information and metadata about a
                  CloudFront function, but not the function's code. To get a
                  function's code, use <code>GetFunction</code>.</p> <p>To get
                  configuration information and metadata about a function, you
                  must provide the function's name and stage. To get these
                  values, you can use <code>ListFunctions</code>.</p>
                tags:
                  - Describe
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/cache-policy/{Id}/config:
              GET:
                summary: GetCachePolicyConfig
                description: >-
                  <p>Gets a cache policy configuration.</p> <p>To get a cache
                  policy configuration, you must provide the policy's
                  identifier. If the cache policy is attached to a
                  distribution's cache behavior, you can get the policy's
                  identifier using <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the cache policy is not
                  attached to a cache behavior, you can get the identifier using
                  <code>ListCachePolicies</code>.</p>
                tags:
                  - Get
                  - Cache
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/origin-access-identity/cloudfront/{Id}/config:
              PUT:
                summary: UpdateCloudFrontOriginAccessIdentity
                description: <p>Update an origin access identity.</p>
                tags:
                  - Update
                  - Cloud
                  - Front
                  - Origin
                  - Access
                  - Identity
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/continuous-deployment-policy/{Id}/config:
              GET:
                summary: GetContinuousDeploymentPolicyConfig
                description: >-
                  <p>Gets configuration information about a continuous
                  deployment policy.</p>
                tags:
                  - Get
                  - Continuous
                  - Deployments
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/distribution/{Id}/config:
              PUT:
                summary: UpdateDistribution
                description: >-
                  <p>Updates the configuration for a CloudFront
                  distribution.</p> <p>The update process includes getting the
                  current distribution configuration, updating it to make your
                  changes, and then submitting an
                  <code>UpdateDistribution</code> request to make the
                  updates.</p> <p> <b>To update a web distribution using the
                  CloudFront API</b> </p> <ol> <li> <p>Use
                  <code>GetDistributionConfig</code> to get the current
                  configuration, including the version identifier
                  (<code>ETag</code>).</p> </li> <li> <p>Update the distribution
                  configuration that was returned in the response. Note the
                  following important requirements and restrictions:</p> <ul>
                  <li> <p>You must rename the <code>ETag</code> field to
                  <code>IfMatch</code>, leaving the value unchanged. (Set the
                  value of <code>IfMatch</code> to the value of
                  <code>ETag</code>, then remove the <code>ETag</code>
                  field.)</p> </li> <li> <p>You can't change the value of
                  <code>CallerReference</code>.</p> </li> </ul> </li> <li>
                  <p>Submit an <code>UpdateDistribution</code> request,
                  providing the distribution configuration. The new
                  configuration replaces the existing configuration. The values
                  that you specify in an <code>UpdateDistribution</code> request
                  are not merged into your existing configuration. Make sure to
                  include all fields: the ones that you modified and also the
                  ones that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/field-level-encryption/{Id}/config:
              PUT:
                summary: UpdateFieldLevelEncryptionConfig
                description: <p>Update a field-level encryption configuration.</p>
                tags:
                  - Update
                  - Fields
                  - Levels
                  - Encryption
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/field-level-encryption-profile/{Id}/config:
              PUT:
                summary: UpdateFieldLevelEncryptionProfile
                description: <p>Update a field-level encryption profile.</p>
                tags:
                  - Update
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/distribution/{DistributionId}/invalidation/{Id}:
              GET:
                summary: GetInvalidation
                description: <p>Get the information about an invalidation.</p>
                tags:
                  - Get
                  - Invalidations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/key-group/{Id}/config:
              GET:
                summary: GetKeyGroupConfig
                description: >-
                  <p>Gets a key group configuration.</p> <p>To get a key group
                  configuration, you must provide the key group's identifier. If
                  the key group is referenced in a distribution's cache
                  behavior, you can get the key group's identifier using
                  <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the key group is not
                  referenced in a cache behavior, you can get the identifier
                  using <code>ListKeyGroups</code>.</p>
                tags:
                  - Get
                  - Keys
                  - Group
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/origin-access-control/{Id}/config:
              PUT:
                summary: UpdateOriginAccessControl
                description: <p>Updates a CloudFront origin access control.</p>
                tags:
                  - Update
                  - Origin
                  - Access
                  - Control
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/origin-request-policy/{Id}/config:
              GET:
                summary: GetOriginRequestPolicyConfig
                description: >-
                  <p>Gets an origin request policy configuration.</p> <p>To get
                  an origin request policy configuration, you must provide the
                  policy's identifier. If the origin request policy is attached
                  to a distribution's cache behavior, you can get the policy's
                  identifier using <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the origin request policy is
                  not attached to a cache behavior, you can get the identifier
                  using <code>ListOriginRequestPolicies</code>.</p>
                tags:
                  - Get
                  - Origin
                  - Request
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/public-key/{Id}/config:
              PUT:
                summary: UpdatePublicKey
                description: >-
                  <p>Update public key information. Note that the only value you
                  can change is the comment.</p>
                tags:
                  - Update
                  - Public
                  - Keys
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/get-realtime-log-config/:
              POST:
                summary: GetRealtimeLogConfig
                description: >-
                  <p>Gets a real-time log configuration.</p> <p>To get a
                  real-time log configuration, you can provide the
                  configuration's name or its Amazon Resource Name (ARN). You
                  must provide at least one. If you provide both, CloudFront
                  uses the name to identify the real-time log configuration to
                  get.</p>
                tags:
                  - Get
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
            /2020-05-31/response-headers-policy/{Id}/config:
              GET:
                summary: GetResponseHeadersPolicyConfig
                description: >-
                  <p>Gets a response headers policy configuration.</p> <p>To get
                  a response headers policy configuration, you must provide the
                  policy's identifier. If the response headers policy is
                  attached to a distribution's cache behavior, you can get the
                  policy's identifier using <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the response headers policy
                  is not attached to a cache behavior, you can get the
                  identifier using <code>ListResponseHeadersPolicies</code>.</p>
                tags:
                  - Get
                  - Responses
                  - Headers
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
            /2020-05-31/streaming-distribution/{Id}/config:
              PUT:
                summary: UpdateStreamingDistribution
                description: <p>Update a streaming distribution.</p>
                tags:
                  - Update
                  - Streaming
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
            /2020-05-31/conflicting-alias:
              GET:
                summary: ListConflictingAliases
                description: >-
                  <p>Gets a list of aliases (also called CNAMEs or alternate
                  domain names) that conflict or overlap with the provided
                  alias, and the associated CloudFront distributions and Amazon
                  Web Services accounts for each conflicting alias. In the
                  returned list, the distribution and account IDs are partially
                  hidden, which allows you to identify the distributions and
                  accounts that you own, but helps to protect the information of
                  ones that you don't own.</p> <p>Use this operation to find
                  aliases that are in use in CloudFront that conflict or overlap
                  with the provided alias. For example, if you provide
                  <code>www.example.com</code> as input, the returned list can
                  include <code>www.example.com</code> and the overlapping
                  wildcard alternate domain name (<code>*.example.com</code>),
                  if they exist. If you provide <code>*.example.com</code> as
                  input, the returned list can include
                  <code>*.example.com</code> and any alternate domain names
                  covered by that wildcard (for example,
                  <code>www.example.com</code>, <code>test.example.com</code>,
                  <code>dev.example.com</code>, and so on), if they exist.</p>
                  <p>To list conflicting aliases, you provide the alias to
                  search and the ID of a distribution in your account that has
                  an attached SSL/TLS certificate that includes the provided
                  alias. For more information, including how to set up the
                  distribution and certificate, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/CNAMEs.html#alternate-domain-names-move">Moving
                  an alternate domain name to a different distribution</a> in
                  the <i>Amazon CloudFront Developer Guide</i>.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Conflicting
                  - Aliases
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
            /2020-05-31/distributionsByCachePolicyId/{CachePolicyId}:
              GET:
                summary: ListDistributionsByCachePolicyId
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that's associated with the specified cache
                  policy.</p> <p>You can optionally specify the maximum number
                  of items to receive in the response. If the total number of
                  items in the list exceeds the maximum that you specify, or the
                  default maximum, the response is paginated. To get the next
                  page of items, send a subsequent request that specifies the
                  <code>NextMarker</code> value from the current response as the
                  <code>Marker</code> value in the subsequent request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Cache
                  - Policies
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByKeyGroupId/{KeyGroupId}:
              GET:
                summary: ListDistributionsByKeyGroup
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that references the specified key group.</p>
                  <p>You can optionally specify the maximum number of items to
                  receive in the response. If the total number of items in the
                  list exceeds the maximum that you specify, or the default
                  maximum, the response is paginated. To get the next page of
                  items, send a subsequent request that specifies the
                  <code>NextMarker</code> value from the current response as the
                  <code>Marker</code> value in the subsequent request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Keys
                  - Group
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByOriginRequestPolicyId/{OriginRequestPolicyId}:
              GET:
                summary: ListDistributionsByOriginRequestPolicyId
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that's associated with the specified origin
                  request policy.</p> <p>You can optionally specify the maximum
                  number of items to receive in the response. If the total
                  number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Origin
                  - Request
                  - Policies
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByRealtimeLogConfig/:
              POST:
                summary: ListDistributionsByRealtimeLogConfig
                description: >-
                  <p>Gets a list of distributions that have a cache behavior
                  that's associated with the specified real-time log
                  configuration.</p> <p>You can specify the real-time log
                  configuration by its name or its Amazon Resource Name (ARN).
                  You must provide at least one. If you provide both, CloudFront
                  uses the name to identify the real-time log configuration to
                  list distributions for.</p> <p>You can optionally specify the
                  maximum number of items to receive in the response. If the
                  total number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByResponseHeadersPolicyId/{ResponseHeadersPolicyId}:
              GET:
                summary: ListDistributionsByResponseHeadersPolicyId
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that's associated with the specified response
                  headers policy.</p> <p>You can optionally specify the maximum
                  number of items to receive in the response. If the total
                  number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Responses
                  - Headers
                  - Policies
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByWebACLId/{WebACLId}:
              GET:
                summary: ListDistributionsByWebACLId
                description: >-
                  <p>List the distributions that are associated with a specified
                  WAF web ACL.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Web
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
            /2020-05-31/key-value-store:
              GET:
                summary: ListKeyValueStores
                description: <p>Specifies the Key Value Stores to list.</p>
                tags:
                  - Lists
                  - Keys
                  - Value
                  - Stores
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
            /2020-05-31/tagging:
              GET:
                summary: ListTagsForResource
                description: <p>List tags for a CloudFront resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
            /2020-05-31/function/{Name}/publish:
              POST:
                summary: PublishFunction
                description: >-
                  <p>Publishes a CloudFront function by copying the function
                  code from the <code>DEVELOPMENT</code> stage to
                  <code>LIVE</code>. This automatically updates all cache
                  behaviors that are using this function to use the newly
                  published copy in the <code>LIVE</code> stage.</p> <p>When a
                  function is published to the <code>LIVE</code> stage, you can
                  attach the function to a distribution's cache behavior, using
                  the function's Amazon Resource Name (ARN).</p> <p>To publish a
                  function, you must provide the function's name and version
                  (<code>ETag</code> value). To get these values, you can use
                  <code>ListFunctions</code> and
                  <code>DescribeFunction</code>.</p>
                tags:
                  - Publish
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
            /2020-05-31/tagging?Operation=Tag:
              POST:
                summary: TagResource
                description: <p>Add tags to a CloudFront resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
            /2020-05-31/function/{Name}/test:
              POST:
                summary: TestFunction
                description: >-
                  <p>Tests a CloudFront function.</p> <p>To test a function, you
                  provide an <i>event object</i> that represents an HTTP request
                  or response that your CloudFront distribution could receive in
                  production. CloudFront runs the function, passing it the event
                  object that you provided, and returns the function's result
                  (the modified event object) in the response. The response also
                  contains function logs and error messages, if any exist. For
                  more information about testing functions, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/managing-functions.html#test-function">Testing
                  functions</a> in the <i>Amazon CloudFront Developer
                  Guide</i>.</p> <p>To test a function, you provide the
                  function's name and version (<code>ETag</code> value) along
                  with the event object. To get the function's name and version,
                  you can use <code>ListFunctions</code> and
                  <code>DescribeFunction</code>.</p>
                tags:
                  - Tests
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
            /2020-05-31/tagging?Operation=Untag:
              POST:
                summary: UntagResource
                description: <p>Remove tags from a CloudFront resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
                  - Untag
            /2020-05-31/distribution/{Id}/promote-staging-config:
              PUT:
                summary: UpdateDistributionWithStagingConfig
                description: >-
                  <p>Copies the staging distribution's configuration to its
                  corresponding primary distribution. The primary distribution
                  retains its <code>Aliases</code> (also known as alternate
                  domain names or CNAMEs) and
                  <code>ContinuousDeploymentPolicyId</code> value, but otherwise
                  its configuration is overwritten to match the staging
                  distribution.</p> <p>You can use this operation in a
                  continuous deployment workflow after you have tested
                  configuration changes on the staging distribution. After using
                  a continuous deployment policy to move a portion of your
                  domain name's traffic to the staging distribution and
                  verifying that it works as intended, you can use this
                  operation to copy the staging distribution's configuration to
                  the primary distribution. This action will disable the
                  continuous deployment policy and move your domain's traffic
                  back to the primary distribution.</p> <p>This API operation
                  requires the following IAM permissions:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_GetDistribution.html">GetDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_UpdateDistribution.html">UpdateDistribution</a>
                  </p> </li> </ul>
                tags:
                  - Update
                  - Distributions
                  - null
                  - Staging
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
                  - Untag
                  - Promote
                  - Staging
            /2020-05-31/realtime-log-config/:
              PUT:
                summary: UpdateRealtimeLogConfig
                description: >-
                  <p>Updates a real-time log configuration.</p> <p>When you
                  update a real-time log configuration, all the parameters are
                  updated with the values provided in the request. You cannot
                  update some parameters independent of others. To update a
                  real-time log configuration:</p> <ol> <li> <p>Call
                  <code>GetRealtimeLogConfig</code> to get the current real-time
                  log configuration.</p> </li> <li> <p>Locally modify the
                  parameters in the real-time log configuration that you want to
                  update.</p> </li> <li> <p>Call this API
                  (<code>UpdateRealtimeLogConfig</code>) by providing the entire
                  real-time log configuration, including the parameters that you
                  modified and those that you didn't.</p> </li> </ol> <p>You
                  cannot update a real-time log configuration's
                  <code>Name</code> or <code>ARN</
                tags:
                  - Update
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - null
                  - null
                  - null
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - null
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
                  - Untag
                  - Promote
                  - Staging
    overlays:
      - type: APIs.io Search
        url: overlays/cloudfront-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudfront-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudfront
  - name: controltower
    description: >-
      <p>These interfaces allow you to apply the Amazon Web Services library of
      pre-defined <i>controls</i> to your organizational units,
      programmatically. In Amazon Web Services Control Tower, the terms
      "control" and "guardrail" are synonyms.</p> <p>To call these APIs, you'll
      need to know:</p> <ul> <li> <p>the <code>controlIdentifier</code> for the
      control--or guardrail--you are targeting.</p> </li> <li> <p>the ARN
      associated with the target organizational unit (OU), which we call the
      <code>targetIdentifier</code>.</p> </li> <li> <p>the ARN associated with a
      resource that you wish to tag or untag.</p> </li> </ul> <p> <b>To get the
      <code>controlIdentifier</code> for your Amazon Web Services Control Tower
      control:</b> </p> <p>The <code>controlIdentifier</code> is an ARN that is
      specified for each control. You can view the
      <code>controlIdentifier</code> in the console on the <b>Control
      details</b> page, as well as in the documentation.</p> <p>The
      <code>controlIdentifier</code> is unique in each Amazon Web Services
      Region for each control. You can find the <code>controlIdentifier</code>
      for each Region and control in the <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-metadata-tables.html">Tables
      of control metadata</a> in the <i>Amazon Web Services Control Tower User
      Guide.</i> </p> <p>A quick-reference list of control identifers for the
      Amazon Web Services Control Tower legacy <i>Strongly recommended</i> and
      <i>Elective</i> controls is given in <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-identifiers.html.html">Resource
      identifiers for APIs and controls</a> in the <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-identifiers.html">Controls
      reference guide section</a> of the <i>Amazon Web Services Control Tower
      User Guide</i>. Remember that <i>Mandatory</i> controls cannot be added or
      removed.</p> <note> <p> <b>ARN format:</b>
      <code>arn:aws:controltower:{REGION}::control/{CONTROL_NAME}</code> </p>
      <p> <b>Example:</b> </p> <p>
      <code>arn:aws:controltower:us-west-2::control/AWS-GR_AUTOSCALING_LAUNCH_CONFIG_PUBLIC_IP_DISABLED</code>
      </p> </note> <p> <b>To get the <code>targetIdentifier</code>:</b> </p>
      <p>The <code>targetIdentifier</code> is the ARN for an OU.</p> <p>In the
      Amazon Web Services Organizations console, you can find the ARN for the OU
      on the <b>Organizational unit details</b> page associated with that
      OU.</p> <note> <p> <b>OU ARN format:</b> </p> <p>
      <code>arn:${Partition}:organizations::${MasterAccountId}:ou/o-${OrganizationId}/ou-${OrganizationalUnitId}</code>
      </p> </note> <p class="title"> <b>Details and examples</b> </p> <ul> <li>
      <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">Control
      API input and output examples with CLI</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/enable-controls.html">Enable
      controls with CloudFormation</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-metadata-tables.html">Control
      metadata tables</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-identifiers.html">List
      of identifiers for legacy controls</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/controls.html">Controls
      reference guide</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/controls-reference.html">Controls
      library groupings</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/creating-resources-with-cloudformation.html">Creating
      Amazon Web Services Control Tower resources with Amazon Web Services
      CloudFormation</a> </p> </li> </ul> <p>To view the open source resource
      repository on GitHub, see <a
      href="https://github.com/aws-cloudformation/aws-cloudformation-resource-providers-controltower">aws-cloudformation/aws-cloudformation-resource-providers-controltower</a>
      </p> <p> <b>Recording API Requests</b> </p> <p>Amazon Web Services Control
      Tower supports Amazon Web Services CloudTrail, a service that records
      Amazon Web Services API calls for your Amazon Web Services account and
      delivers log files to an Amazon S3 bucket. By using information collected
      by CloudTrail, you can determine which requests the Amazon Web Services
      Control Tower service received, who made the request and when, and so on.
      For more about Amazon Web Services Control Tower and its support for
      CloudTrail, see <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/logging-using-cloudtrail.html">Logging
      Amazon Web Services Control Tower Actions with Amazon Web Services
      CloudTrail</a> in the Amazon Web Services Control Tower User Guide. To
      learn more about CloudTrail, including how to turn it on and find your log
      files, see the Amazon Web Services CloudTrail User Guide.</p>
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
            title: controltower
          paths:
            /create-landingzone:
              POST:
                summary: CreateLandingZone
                description: >-
                  <p>Creates a new landing zone. This API call starts an
                  asynchronous operation that creates and configures a landing
                  zone, based on the parameters specified in the manifest JSON
                  file.</p>
                tags:
                  - Create
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
            /delete-landingzone:
              POST:
                summary: DeleteLandingZone
                description: >-
                  <p>Decommissions a landing zone. This API call starts an
                  asynchronous operation that deletes Amazon Web Services
                  Control Tower resources deployed in accounts managed by Amazon
                  Web Services Control Tower.</p>
                tags:
                  - Delete
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
            /disable-baseline:
              POST:
                summary: DisableBaseline
                description: >-
                  <p>Disable an <code>EnabledBaseline</code> resource on the
                  specified Target. This API starts an asynchronous operation to
                  remove all resources deployed as part of the baseline
                  enablement. The resource will vary depending on the enabled
                  baseline.</p>
                tags:
                  - Disable
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
            /disable-control:
              POST:
                summary: DisableControl
                description: >-
                  <p>This API call turns off a control. It starts an
                  asynchronous operation that deletes AWS resources on the
                  specified organizational unit and the accounts it contains.
                  The resources will vary according to the control that you
                  specify. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Disable
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
            /enable-baseline:
              POST:
                summary: EnableBaseline
                description: >-
                  <p>Enable (apply) a <code>Baseline</code> to a Target. This
                  API starts an asynchronous operation to deploy resources
                  specified by the <code>Baseline</code> to the specified
                  Target.</p>
                tags:
                  - Enable
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
            /enable-control:
              POST:
                summary: EnableControl
                description: >-
                  <p>This API call activates a control. It starts an
                  asynchronous operation that creates Amazon Web Services
                  resources on the specified organizational unit and the
                  accounts it contains. The resources created will vary
                  according to the control that you specify. For usage examples,
                  see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Enable
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
            /get-baseline:
              POST:
                summary: GetBaseline
                description: >-
                  <p>Retrieve details about an existing <code>Baseline</code>
                  resource by specifying its identifier.</p>
                tags:
                  - Get
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
            /get-baseline-operation:
              POST:
                summary: GetBaselineOperation
                description: >-
                  <p>Returns the details of an asynchronous baseline operation,
                  as initiated by any of these APIs:
                  <code>EnableBaseline</code>, <code>DisableBaseline</code>,
                  <code>UpdateEnabledBaseline</code>,
                  <code>ResetEnabledBaseline</code>. A status message is
                  displayed in case of operation failure.</p>
                tags:
                  - Get
                  - Baselines
                  - Operation
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
            /get-control-operation:
              POST:
                summary: GetControlOperation
                description: >-
                  <p>Returns the status of a particular
                  <code>EnableControl</code> or <code>DisableControl</code>
                  operation. Displays a message in case of error. Details for an
                  operation are available for 90 days. For usage examples, see
                  <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Get
                  - Control
                  - Operation
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
            /get-enabled-baseline:
              POST:
                summary: GetEnabledBaseline
                description: >-
                  <p>Retrieve details of an <code>EnabledBaseline</code>
                  resource by specifying its identifier.</p>
                tags:
                  - Get
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /get-enabled-control:
              POST:
                summary: GetEnabledControl
                description: >-
                  <p>Retrieves details about an enabled control. For usage
                  examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Get
                  - Enabled
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /get-landingzone:
              POST:
                summary: GetLandingZone
                description: >-
                  <p>Returns details about the landing zone. Displays a message
                  in case of error.</p>
                tags:
                  - Get
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /get-landingzone-operation:
              POST:
                summary: GetLandingZoneOperation
                description: >-
                  <p>Returns the status of the specified landing zone operation.
                  Details for an operation are available for 60 days.</p>
                tags:
                  - Get
                  - Landing
                  - Zones
                  - Operation
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /list-baselines:
              POST:
                summary: ListBaselines
                description: <p>Returns a summary list of all available baselines.</p>
                tags:
                  - Lists
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
            /list-enabled-baselines:
              POST:
                summary: ListEnabledBaselines
                description: >-
                  <p>Returns a list of summaries describing
                  <code>EnabledBaseline</code> resources. You can filter the
                  list by the corresponding <code>Baseline</code> or
                  <code>Target</code> of the <code>EnabledBaseline</code>
                  resources.</p>
                tags:
                  - Lists
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
            /list-enabled-controls:
              POST:
                summary: ListEnabledControls
                description: >-
                  <p>Lists the controls enabled by Amazon Web Services Control
                  Tower on the specified organizational unit and the accounts it
                  contains. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Lists
                  - Enabled
                  - Controls
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
            /list-landingzones:
              POST:
                summary: ListLandingZones
                description: >-
                  <p>Returns the landing zone ARN for the landing zone deployed
                  in your managed account. This API also creates an ARN for
                  existing accounts that do not yet have a landing zone ARN.
                  </p> <p>Returns one landing zone ARN.</p>
                tags:
                  - Lists
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes tags from a resource. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Untag
                  - Resources
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
            /reset-enabled-baseline:
              POST:
                summary: ResetEnabledBaseline
                description: >-
                  <p>Re-enables an <code>EnabledBaseline</code> resource. For
                  example, this API can re-apply the existing
                  <code>Baseline</code> after a new member account is moved to
                  the target OU.</p>
                tags:
                  - Reset
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
            /reset-landingzone:
              POST:
                summary: ResetLandingZone
                description: >-
                  <p>This API call resets a landing zone. It starts an
                  asynchronous operation that resets the landing zone to the
                  parameters specified in its original configuration.</p>
                tags:
                  - Reset
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
            /update-enabled-baseline:
              POST:
                summary: UpdateEnabledBaseline
                description: >-
                  <p>Updates an <code>EnabledBaseline</code> resource's applied
                  parameters or version.</p>
                tags:
                  - Update
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
                  - Update
            /update-enabled-control:
              POST:
                summary: UpdateEnabledControl
                description: >-
                  <p> Updates the configuration of an already enabled
                  control.</p> <p>If the enabled control shows an
                  <code>EnablementStatus</code> of SUCCEEDED, supply parameters
                  that are different from the currently configured parameters.
                  Otherwise, Amazon Web Services Control Tower will not accept
                  the request.</p> <p>If the enabled control shows an
                  <code>EnablementStatus</code> of FAILED, Amazon Web Services
                  Control Tower will update the control to match any valid
                  parameters that you supply.</p> <p>If the
                  <code>DriftSummary</code> status for the control shows as
                  DRIFTED, you cannot call this API. Instead, you can update the
                  control by calling <code>DisableControl</code> and again
                  calling <code>EnableControl</code>, or you can run an
                  extending governance operation. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i> </a>
                  </p>
                tags:
                  - Update
                  - Enabled
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
                  - Update
            /update-landingzone:
              POST:
                summary: UpdateLandingZone
                description: >-
                  <p>This API call updates the landing zone. It starts an
                  asynchronous operation that updates the landing zone based on
                  the new landing zone version, or on the changed parameters
                  specified in the updated manifest
                tags:
                  - Update
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/controltower-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/controltower-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:controltower
  - name: qbusiness
    description: >-
      <note> <p>Amazon Q is in preview release and is subject to change.</p>
      </note> <p>This is the <i>Amazon Q (for business use)</i> API Reference.
      Amazon Q is a fully managed, generative-AI powered enterprise chat
      assistant that you can deploy within your organization. Amazon Q enhances
      employee productivity by supporting key tasks such as question-answering,
      knowledge discovery, writing email messages, summarizing text, drafting
      document outlines, and brainstorming ideas. Users ask questions of Amazon
      Q and get answers that are presented in a conversational manner. For an
      introduction to the service, see the <a
      href="https://docs.aws.amazon.com/amazonq/latest/business-use-dg/what-is.html">
      <i>Amazon Q (for business use) Developer Guide</i> </a>.</p> <p>For an
      overview of the Amazon Q APIs, see <a
      href="https://docs.aws.amazon.com/amazonq/latest/business-use-dg/api-ref.html#api-overview">Overview
      of Amazon Q API operations</a>.</p> <p>For information about the IAM
      access control permissions you need to use this API, see <a
      href="https://docs.aws.amazon.com/amazonq/latest/business-use-dg/iam-roles.html">IAM
      roles for Amazon Q</a> in the <i>Amazon Q (for business use) Developer
      Guide</i>.</p> <p>You can use the following AWS SDKs to access Amazon Q
      APIs:</p> <ul> <li> <p> <a
      href="https://docs.aws.amazon.com/sdk-for-cpp">AWS SDK for C++</a> </p>
      </li> <li> <p> <a href="https://docs.aws.amazon.com/sdk-for-go">AWS SDK
      for Go</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/sdk-for-java">AWS SDK for Java</a> </p>
      </li> <li> <p> <a
      href="https://docs.aws.amazon.com/sdk-for-javascript">AWS SDK for
      JavaScript</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/sdk-for-net">AWS SDK for .NET</a> </p>
      </li> <li> <p> <a href="https://docs.aws.amazon.com/pythonsdk">AWS SDK for
      Python (Boto3)</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/sdk-for-ruby">AWS SDK for Ruby</a> </p>
      </li> </ul> <p>The following resources provide additional information
      about using the Amazon Q API:</p> <ul> <li> <p> <i> <a
      href="https://docs.aws.amazon.com/amazonq/latest/business-use-dg/setting-up.html">Setting
      up for Amazon Q</a> </i> </p> </li> <li> <p> <i> <a
      href="https://awscli.amazonaws.com/v2/documentation/api/latest/reference/qbusiness/index.html">Amazon
      Q CLI Reference</a> </i> </p> </li> <li> <p> <i> <a
      href="https://docs.aws.amazon.com/general/latest/gr/amazonq.html">Amazon
      Web Services General Reference</a> </i> </p> </li> </ul>
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
            title: qbusiness
          paths:
            /applications/{applicationId}/indices/{indexId}/documents/delete:
              POST:
                summary: BatchDeleteDocument
                description: >-
                  <p>Asynchronously deletes one or more documents added using
                  the <code>BatchPutDocument</code> API from an Amazon Q
                  index.</p> <p>You can see the progress of the deletion, and
                  any error messages related to the process, by using
                  CloudWatch.</p>
                tags:
                  - Batches
                  - Delete
                  - Document
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
            /applications/{applicationId}/indices/{indexId}/documents:
              POST:
                summary: BatchPutDocument
                description: >-
                  <p>Adds one or more documents to an Amazon Q index.</p> <p>You
                  use this API to:</p> <ul> <li> <p>ingest your structured and
                  unstructured documents and documents stored in an Amazon S3
                  bucket into an Amazon Q index.</p> </li> <li> <p>add custom
                  attributes to documents in an Amazon Q index.</p> </li> <li>
                  <p>attach an access control list to the documents added to an
                  Amazon Q index.</p> </li> </ul> <p>You can see the progress of
                  the deletion, and any error messages related to the process,
                  by using CloudWatch.</p>
                tags:
                  - Batches
                  - Put
                  - Document
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
            /applications/{applicationId}/conversations?sync:
              POST:
                summary: ChatSync
                description: >-
                  <p>Starts or continues a non-streaming Amazon Q
                  conversation.</p>
                tags:
                  - Chat
                  - Sync
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
            /applications:
              GET:
                summary: ListApplications
                description: <p>Lists Amazon Q applications.</p>
                tags:
                  - Lists
                  - Applications
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
            /applications/{applicationId}/indices/{indexId}/datasources:
              GET:
                summary: ListDataSources
                description: >-
                  <p>Lists the Amazon Q data source connectors that you have
                  created.</p>
                tags:
                  - Lists
                  - Data
                  - Sources
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
            /applications/{applicationId}/indices:
              GET:
                summary: ListIndices
                description: <p>Lists the Amazon Q indices you have created.</p>
                tags:
                  - Lists
                  - Indices
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
            /applications/{applicationId}/plugins:
              GET:
                summary: ListPlugins
                description: <p>Lists configured Amazon Q plugins.</p>
                tags:
                  - Lists
                  - Plugins
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
            /applications/{applicationId}/retrievers:
              GET:
                summary: ListRetrievers
                description: <p>Lists the retriever used by an Amazon Q application.</p>
                tags:
                  - Lists
                  - Retrievers
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
            /applications/{applicationId}/users:
              POST:
                summary: CreateUser
                description: >-
                  <p>Creates a universally unique identifier (UUID) mapped to a
                  list of local user ids within an application.</p>
                tags:
                  - Create
                  - Users
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
            /applications/{applicationId}/experiences:
              GET:
                summary: ListWebExperiences
                description: <p>Lists one or more Amazon Q Web Experiences.</p>
                tags:
                  - Lists
                  - Web
                  - Experiences
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
            /applications/{applicationId}:
              PUT:
                summary: UpdateApplication
                description: <p>Updates an existing Amazon Q application.</p>
                tags:
                  - Update
                  - Applications
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
            /applications/{applicationId}/chatcontrols:
              PATCH:
                summary: UpdateChatControlsConfiguration
                description: >-
                  <p>Updates an set of chat controls configured for an existing
                  Amazon Q application.</p>
                tags:
                  - Update
                  - Chat
                  - Controls
                  - Configurations
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
            /applications/{applicationId}/conversations/{conversationId}:
              GET:
                summary: ListMessages
                description: >-
                  <p>Gets a list of messages associated with an Amazon Q web
                  experience.</p>
                tags:
                  - Lists
                  - Messages
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
            /applications/{applicationId}/indices/{indexId}/datasources/{dataSourceId}:
              PUT:
                summary: UpdateDataSource
                description: <p>Updates an existing Amazon Q data source connector.</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
            /applications/{applicationId}/indices/{indexId}/groups/{groupName}:
              GET:
                summary: GetGroup
                description: <p>Describes a group by group name.</p>
                tags:
                  - Get
                  - Group
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
            /applications/{applicationId}/indices/{indexId}:
              PUT:
                summary: UpdateIndex
                description: <p>Updates an Amazon Q index.</p>
                tags:
                  - Update
                  - Index
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
            /applications/{applicationId}/plugins/{pluginId}:
              PUT:
                summary: UpdatePlugin
                description: <p>Updates an Amazon Q plugin.</p>
                tags:
                  - Update
                  - Plugins
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
            /applications/{applicationId}/retrievers/{retrieverId}:
              PUT:
                summary: UpdateRetriever
                description: >-
                  <p>Updates the retriever used for your Amazon Q
                  application.</p>
                tags:
                  - Update
                  - Retrievers
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
            /applications/{applicationId}/users/{userId}:
              PUT:
                summary: UpdateUser
                description: <p>Updates a information associated with a user id.</p>
                tags:
                  - Update
                  - Users
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
            /applications/{applicationId}/experiences/{webExperienceId}:
              PUT:
                summary: UpdateWebExperience
                description: <p>Updates an Amazon Q web experience. </p>
                tags:
                  - Update
                  - Web
                  - Experience
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
            /applications/{applicationId}/conversations:
              GET:
                summary: ListConversations
                description: <p>Lists one or more Amazon Q conversations.</p>
                tags:
                  - Lists
                  - Conversations
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
            /applications/{applicationId}/indices/{indexId}/datasources/{dataSourceId}/syncjobs:
              GET:
                summary: ListDataSourceSyncJobs
                description: >-
                  <p>Get information about an Amazon Q data source connector
                  synchronization.</p>
                tags:
                  - Lists
                  - Data
                  - Source
                  - Sync
                  - Jobs
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
            /applications/{applicationId}/index/{indexId}/documents:
              GET:
                summary: ListDocuments
                description: <p>A list of documents attached to an index.</p>
                tags:
                  - Lists
                  - Documents
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
            /applications/{applicationId}/indices/{indexId}/groups:
              PUT:
                summary: PutGroup
                description: >-
                  <p>Create, or updates, a mapping of users—who have access to a
                  document—to groups.</p> <p>You can also map sub groups to
                  groups. For example, the group "Company Intellectual Property
                  Teams" includes sub groups "Research" and "Engineering". These
                  sub groups include their own list of users or people who work
                  in these teams. Only users who work in research and
                  engineering, and therefore belong in the intellectual property
                  group, can see top-secret company documents in their Amazon Q
                  chat results.</p>
                tags:
                  - Put
                  - Group
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
            /v1/tags/{resourceARN}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes a tag from an Amazon Q application or a data
                  source.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
                  - V1
                  - Tags
                  - ResourceARN
            /applications/{applicationId}/conversations/{conversationId}/messages/{messageId}/feedback:
              POST:
                summary: PutFeedback
                description: >-
                  <p>Enables your end user to to provide feedback on their
                  Amazon Q generated chat responses.</p>
                tags:
                  - Put
                  - Feedback
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
                  - V1
                  - Tags
                  - ResourceARN
                  - Messages
                  - Messages
                  - Feedback
            /applications/{applicationId}/indices/{indexId}/datasources/{dataSourceId}/startsync:
              POST:
                summary: StartDataSourceSyncJob
                description: >-
                  <p>Starts a data source connector synchronization job. If a
                  synchronization job is already in progress, Amazon Q returns a
                  <code>ConflictException</code>.</p>
                tags:
                  - Start
                  - Data
                  - Source
                  - Sync
                  - Jobs
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
                  - V1
                  - Tags
                  - ResourceARN
                  - Messages
                  - Messages
                  - Feedback
                  - Start Sync
            /applications/{applicationId}/indices/{indexId}/datasources/{dataSourceId}/stopsync:
              POST:
                summary: StopDataSourceSyncJob
                description: >-
                  <p>Stops an Amazon Q data source connector synchronization job
                  already in pro
                tags:
                  - Stop
                  - Data
                  - Source
                  - Sync
                  - Jobs
                  - Identifiers
                  - Indices
                  - Index
                  - Documents
                  - Delete
                  - Conversations
                  - Applications
                  - Data Source
                  - Plugins
                  - Retrievers
                  - Users
                  - Experiences
                  - Chat Controls
                  - Conversations
                  - Conversations
                  - Data
                  - Source
                  - Groups
                  - Group
                  - Names
                  - Plugins
                  - Retrievers
                  - Users
                  - Web
                  - Experience
                  - Sync Jobs
                  - V1
                  - Tags
                  - ResourceARN
                  - Messages
                  - Messages
                  - Feedback
                  - Start Sync
                  - Stopsy
    overlays:
      - type: APIs.io Search
        url: overlays/qbusiness-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/qbusiness-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:qbusiness
  - name: route53-recovery-control-config
    description: >-
      <p>Recovery Control Configuration API Reference for Amazon Route 53
      Application Recovery Controller</p>
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
            title: route53-recovery-control-config
          paths:
            /cluster:
              GET:
                summary: ListClusters
                description: <p>Returns an array of all the clusters in an account.</p>
                tags:
                  - Lists
                  - Clusters
                  - Cluster
            /controlpanel:
              PUT:
                summary: UpdateControlPanel
                description: >-
                  <p>Updates a control panel. The only update you can make to a
                  control panel is to change the name of the control panel.</p>
                tags:
                  - Update
                  - Control
                  - Panels
                  - Cluster
                  - Control Panels
            /routingcontrol:
              PUT:
                summary: UpdateRoutingControl
                description: >-
                  <p>Updates a routing control. You can only update the name of
                  the routing control. To get or update the routing control
                  state, see the Recovery Cluster (data plane) API actions for
                  Amazon Route 53 Application Recovery Controller.</p>
                tags:
                  - Update
                  - Routing
                  - Control
                  - Cluster
                  - Control Panels
                  - Routing Controls
            /safetyrule:
              PUT:
                summary: UpdateSafetyRule
                description: >-
                  <p>Update a safety rule (an assertion rule or gating rule).
                  You can only update the name and the waiting period for a
                  safety rule. To make other updates, delete the safety rule and
                  create a new one.</p>
                tags:
                  - Update
                  - Safety
                  - Rules
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
            /cluster/{ClusterArn}:
              GET:
                summary: DescribeCluster
                description: >-
                  <p>Display the details about a cluster. The response includes
                  the cluster name, endpoints, status, and Amazon Resource Name
                  (ARN).</p>
                tags:
                  - Describe
                  - Cluster
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
            /controlpanel/{ControlPanelArn}:
              GET:
                summary: DescribeControlPanel
                description: <p>Displays details about a control panel.</p>
                tags:
                  - Describe
                  - Control
                  - Panels
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
            /routingcontrol/{RoutingControlArn}:
              GET:
                summary: DescribeRoutingControl
                description: >-
                  <p>Displays details about a routing control. A routing control
                  has one of two states: ON and OFF. You can map the routing
                  control state to the state of an Amazon Route 53 health check,
                  which can be used to control routing.</p> <p>To get or update
                  the routing control state, see the Recovery Cluster (data
                  plane) API actions for Amazon Route 53 Application Recovery
                  Controller.</p>
                tags:
                  - Describe
                  - Routing
                  - Control
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
            /safetyrule/{SafetyRuleArn}:
              GET:
                summary: DescribeSafetyRule
                description: <p>Returns information about a safety rule.</p>
                tags:
                  - Describe
                  - Safety
                  - Rules
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
            /resourcePolicy/{ResourceArn}:
              GET:
                summary: GetResourcePolicy
                description: >-
                  <p>Get information about the resource policy for a
                  cluster.</p>
                tags:
                  - Get
                  - Resources
                  - Policies
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
                  - Policies
                  - Resources
            /routingcontrol/{RoutingControlArn}/associatedRoute53HealthChecks:
              GET:
                summary: ListAssociatedRoute53HealthChecks
                description: >-
                  <p>Returns an array of all Amazon Route 53 health checks
                  associated with a specific routing control.</p>
                tags:
                  - Lists
                  - Associated
                  - Route53
                  - Health
                  - Checks
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
                  - Policies
                  - Resources
                  - Associated
                  - Route53
                  - Health
                  - Checks
            /controlpanels:
              GET:
                summary: ListControlPanels
                description: >-
                  <p>Returns an array of control panels in an account or in a
                  cluster.</p>
                tags:
                  - Lists
                  - Control
                  - Panels
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
                  - Policies
                  - Resources
                  - Associated
                  - Route53
                  - Health
                  - Checks
                  - Control Panels
            /controlpanel/{ControlPanelArn}/routingcontrols:
              GET:
                summary: ListRoutingControls
                description: >-
                  <p>Returns an array of routing controls for a control panel. A
                  routing control is an Amazon Route 53 Application Recovery
                  Controller construct that has one of two states: ON and OFF.
                  You can map the routing control state to the state of an
                  Amazon Route 53 health check, which can be used to control
                  routing.</p>
                tags:
                  - Lists
                  - Routing
                  - Controls
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
                  - Policies
                  - Resources
                  - Associated
                  - Route53
                  - Health
                  - Checks
                  - Control Panels
                  - Routing Controls
            /controlpanel/{ControlPanelArn}/safetyrules:
              GET:
                summary: ListSafetyRules
                description: >-
                  <p>List the safety rules (the assertion rules and gating
                  rules) that you've defined for the routing controls in a
                  control panel.</p>
                tags:
                  - Lists
                  - Safety
                  - Rules
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
                  - Policies
                  - Resources
                  - Associated
                  - Route53
                  - Health
                  - Checks
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from a res
                tags:
                  - Untag
                  - Resources
                  - Cluster
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
                  - ARN
                  - Control
                  - Panels
                  - Routing
                  - Safety
                  - Rules
                  - Policies
                  - Resources
                  - Associated
                  - Route53
                  - Health
                  - Checks
                  - Control Panels
                  - Routing Controls
                  - Safety Rules
    overlays:
      - type: APIs.io Search
        url: overlays/route53-recovery-control-config-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/route53-recovery-control-config-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53-recovery-control-config
  - name: s3
    description: <p/>
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
            title: s3
          paths:
            /{Bucket}/{Key+}:
              PUT:
                summary: UploadPartCopy
                description: >-
                  <p>Uploads a part by copying data from an existing object as
                  data source. To specify the data source, you add the request
                  header <code>x-amz-copy-source</code> in your request. To
                  specify a byte range, you add the request header
                  <code>x-amz-copy-source-range</code> in your request. </p>
                  <p>For information about maximum and minimum part sizes and
                  other multipart upload specifications, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/qfacts.html">Multipart
                  upload limits</a> in the <i>Amazon S3 User Guide</i>. </p>
                  <note> <p>Instead of copying data from an existing object as
                  part data, you might use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  action to upload new data as a part of an object in your
                  request.</p> </note> <p>You must initiate a multipart upload
                  before you can upload any part. In response to your initiate
                  request, Amazon S3 returns the upload ID, a unique identifier
                  that you must include in your upload part request.</p> <p>For
                  conceptual information about multipart uploads, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html">Uploading
                  Objects Using Multipart Upload</a> in the <i>Amazon S3 User
                  Guide</i>. For information about copying objects using a
                  single atomic action vs. a multipart upload, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/ObjectOperations.html">Operations
                  on Objects</a> in the <i>Amazon S3 User Guide</i>.</p> <note>
                  <p> <b>Directory buckets</b> - For directory buckets, you must
                  make requests for this API operation to the Zonal endpoint.
                  These endpoints support virtual-hosted-style requests in the
                  format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Authentication and
                  authorization</dt> <dd> <p>All <code>UploadPartCopy</code>
                  requests must be authenticated and signed by using IAM
                  credentials (access key ID and secret access key for the IAM
                  identities). All headers with the <code>x-amz-</code> prefix,
                  including <code>x-amz-copy-source</code>, must be signed. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html">REST
                  Authentication</a>.</p> <p> <b>Directory buckets</b> - You
                  must use IAM credentials to authenticate and authorize your
                  access to the <code>UploadPartCopy</code> API operation,
                  instead of using the temporary security credentials through
                  the <code>CreateSession</code> API operation.</p> <p>Amazon
                  Web Services CLI or SDKs handles authentication and
                  authorization on your behalf.</p> </dd> <dt>Permissions</dt>
                  <dd> <p>You must have <code>READ</code> access to the source
                  object and <code>WRITE</code> access to the destination
                  bucket.</p> <ul> <li> <p> <b>General purpose bucket
                  permissions</b> - You must have the permissions in a policy
                  based on the bucket types of your source bucket and
                  destination bucket in an <code>UploadPartCopy</code>
                  operation.</p> <ul> <li> <p>If the source object is in a
                  general purpose bucket, you must have the <b>
                  <code>s3:GetObject</code> </b> permission to read the source
                  object that is being copied. </p> </li> <li> <p>If the
                  destination bucket is a general purpose bucket, you must have
                  the <b> <code>s3:PubObject</code> </b> permission to write the
                  object copy to the destination bucket. </p> </li> </ul> <p>For
                  information about permissions required to use the multipart
                  upload API, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuAndPermissions.html">Multipart
                  Upload and Permissions</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b>Directory bucket
                  permissions</b> - You must have permissions in a bucket policy
                  or an IAM identity-based policy based on the source and
                  destination bucket types in an <code>UploadPartCopy</code>
                  operation.</p> <ul> <li> <p>If the source object that you want
                  to copy is in a directory bucket, you must have the <b>
                  <code>s3express:CreateSession</code> </b> permission in the
                  <code>Action</code> element of a policy to read the object .
                  By default, the session is in the <code>ReadWrite</code> mode.
                  If you want to restrict the access, you can explicitly set the
                  <code>s3express:SessionMode</code> condition key to
                  <code>ReadOnly</code> on the copy source bucket.</p> </li>
                  <li> <p>If the copy destination is a directory bucket, you
                  must have the <b> <code>s3express:CreateSession</code> </b>
                  permission in the <code>Action</code> element of a policy to
                  write the object to the destination. The
                  <code>s3express:SessionMode</code> condition key cannot be set
                  to <code>ReadOnly</code> on the copy destination. </p> </li>
                  </ul> <p>For example policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-example-bucket-policies.html">Example
                  bucket policies for S3 Express One Zone</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-identity-policies.html">Amazon
                  Web Services Identity and Access Management (IAM)
                  identity-based policies for S3 Express One Zone</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> </ul> </dd>
                  <dt>Encryption</dt> <dd> <ul> <li> <p> <b>General purpose
                  buckets </b> - For information about using server-side
                  encryption with customer-provided encryption keys with the
                  <code>UploadPartCopy</code> operation, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html">CopyObject</a>
                  and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>.
                  </p> </li> <li> <p> <b>Directory buckets </b> - For directory
                  buckets, only server-side encryption with Amazon S3 managed
                  keys (SSE-S3) (<code>AES256</code>) is supported.</p> </li>
                  </ul> </dd> <dt>Special errors</dt> <dd> <ul> <li> <p>Error
                  Code: <code>NoSuchUpload</code> </p> <ul> <li> <p>Description:
                  The specified multipart upload does not exist. The upload ID
                  might be invalid, or the multipart upload might have been
                  aborted or completed.</p> </li> <li> <p>HTTP Status Code: 404
                  Not Found</p> </li> </ul> </li> <li> <p>Error Code:
                  <code>InvalidRequest</code> </p> <ul> <li> <p>Description: The
                  specified copy source is not supported as a byte-range copy
                  source.</p> </li> <li> <p>HTTP Status Code: 400 Bad
                  Request</p> </li> </ul> </li> </ul> </dd> <dt>HTTP Host header
                  syntax</dt> <dd> <p> <b>Directory buckets </b> - The HTTP Host
                  header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>UploadPartCopy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateMultipartUpload.html">CreateMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListMultipartUploads.html">ListMultipartUploads</a>
                  </p> </li> </ul>
                tags:
                  - Uploads
                  - Part
                  - Copy
                  - Bucket
                  - Keys
            /{Bucket}:
              GET:
                summary: ListObjects
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns some or all (up to 1,000) of
                  the objects in a bucket. You can use the request parameters as
                  selection criteria to return a subset of the objects in a
                  bucket. A 200 OK response can contain valid or invalid XML. Be
                  sure to design your application to parse the contents of the
                  response and handle it appropriately.</p> <important> <p>This
                  action has been revised. We recommend that you use the newer
                  version, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html">ListObjectsV2</a>,
                  when developing applications. For backward compatibility,
                  Amazon S3 continues to support <code>ListObjects</code>.</p>
                  </important> <p>The following operations are related to
                  <code>ListObjects</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html">ListObjectsV2</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html">ListBuckets</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Objects
                  - Bucket
                  - Keys
            /{Bucket}/{Key+}?uploads:
              POST:
                summary: CreateMultipartUpload
                description: >-
                  <p>This action initiates a multipart upload and returns an
                  upload ID. This upload ID is used to associate all of the
                  parts in the specific multipart upload. You specify this
                  upload ID in each of your subsequent upload part requests (see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>).
                  You also include this upload ID in the final request to either
                  complete or abort the multipart upload request. For more
                  information about multipart uploads, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html">Multipart
                  Upload Overview</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <note> <p>After you initiate a multipart upload and upload one
                  or more parts, to stop being charged for storing the uploaded
                  parts, you must either complete or abort the multipart upload.
                  Amazon S3 frees up the space used to store the parts and stops
                  charging you for storing them only after you either complete
                  or abort a multipart upload. </p> </note> <p>If you have
                  configured a lifecycle rule to abort incomplete multipart
                  uploads, the created multipart upload must be completed within
                  the number of days specified in the bucket lifecycle
                  configuration. Otherwise, the incomplete multipart upload
                  becomes eligible for an abort action and Amazon S3 aborts the
                  multipart upload. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html#mpu-abort-incomplete-mpu-lifecycle-config">Aborting
                  Incomplete Multipart Uploads Using a Bucket Lifecycle
                  Configuration</a>.</p> <note> <ul> <li> <p> <b>Directory
                  buckets </b> - S3 Lifecycle is not supported by directory
                  buckets.</p> </li> <li> <p> <b>Directory buckets </b> - For
                  directory buckets, you must make requests for this API
                  operation to the Zonal endpoint. These endpoints support
                  virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> </ul> </note> <dl> <dt>Request
                  signing</dt> <dd> <p>For request signing, multipart upload is
                  just a series of regular requests. You initiate a multipart
                  upload, send one or more requests to upload parts, and then
                  complete the multipart upload process. You sign each request
                  individually. There is nothing special about signing multipart
                  upload requests. For more information about signing, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">Authenticating
                  Requests (Amazon Web Services Signature Version 4)</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </dd> <dt>Permissions</dt>
                  <dd> <ul> <li> <p> <b>General purpose bucket permissions</b> -
                  For information about the permissions required to use the
                  multipart upload API, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuAndPermissions.html">Multipart
                  upload and permissions</a> in the <i>Amazon S3 User Guide</i>.
                  </p> <p>To perform a multipart upload with encryption by using
                  an Amazon Web Services KMS key, the requester must have
                  permission to the <code>kms:Decrypt</code> and
                  <code>kms:GenerateDataKey*</code> actions on the key. These
                  permissions are required because Amazon S3 must decrypt and
                  read data from the encrypted file parts before it completes
                  the multipart upload. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpuoverview.html#mpuAndPermissions">Multipart
                  upload API and permissions</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html">Protecting
                  data using server-side encryption with Amazon Web Services
                  KMS</a> in the <i>Amazon S3 User Guide</i>.</p> </li> <li> <p>
                  <b>Directory bucket permissions</b> - To grant access to this
                  API operation on a directory bucket, we recommend that you use
                  the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Encryption</dt> <dd> <ul> <li> <p> <b>General purpose
                  buckets</b> - Server-side encryption is for data encryption at
                  rest. Amazon S3 encrypts your data as it writes it to disks in
                  its data centers and decrypts it when you access it. Amazon S3
                  automatically encrypts all new objects that are uploaded to an
                  S3 bucket. When doing a multipart upload, if you don't specify
                  encryption information in your request, the encryption setting
                  of the uploaded parts is set to the default encryption
                  configuration of the destination bucket. By default, all
                  buckets have a base level of encryption configuration that
                  uses server-side encryption with Amazon S3 managed keys
                  (SSE-S3). If the destination bucket has a default encryption
                  configuration that uses server-side encryption with an Key
                  Management Service (KMS) key (SSE-KMS), or a customer-provided
                  encryption key (SSE-C), Amazon S3 uses the corresponding KMS
                  key, or a customer-provided key to encrypt the uploaded parts.
                  When you perform a CreateMultipartUpload operation, if you
                  want to use a different type of encryption setting for the
                  uploaded parts, you can request that Amazon S3 encrypts the
                  object with a different encryption key (such as an Amazon S3
                  managed key, a KMS key, or a customer-provided key). When the
                  encryption setting in your request is different from the
                  default encryption configuration of the destination bucket,
                  the encryption setting in your request takes precedence. If
                  you choose to provide your own encryption key, the request
                  headers you provide in <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPartCopy.html">UploadPartCopy</a>
                  requests must match the headers you used in the
                  <code>CreateMultipartUpload</code> request.</p> <ul> <li>
                  <p>Use KMS keys (SSE-KMS) that include the Amazon Web Services
                  managed key (<code>aws/s3</code>) and KMS customer managed
                  keys stored in Key Management Service (KMS) – If you want
                  Amazon Web Services to manage the keys used to encrypt data,
                  specify the following headers in the request.</p> <ul> <li>
                  <p> <code>x-amz-server-side-encryption</code> </p> </li> <li>
                  <p> <code>x-amz-server-side-encryption-aws-kms-key-id</code>
                  </p> </li> <li> <p>
                  <code>x-amz-server-side-encryption-context</code> </p> </li>
                  </ul> <note> <ul> <li> <p>If you specify
                  <code>x-amz-server-side-encryption:aws:kms</code>, but don't
                  provide
                  <code>x-amz-server-side-encryption-aws-kms-key-id</code>,
                  Amazon S3 uses the Amazon Web Services managed key
                  (<code>aws/s3</code> key) in KMS to protect the data.</p>
                  </li> <li> <p>To perform a multipart upload with encryption by
                  using an Amazon Web Services KMS key, the requester must have
                  permission to the <code>kms:Decrypt</code> and
                  <code>kms:GenerateDataKey*</code> actions on the key. These
                  permissions are required because Amazon S3 must decrypt and
                  read data from the encrypted file parts before it completes
                  the multipart upload. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpuoverview.html#mpuAndPermissions">Multipart
                  upload API and permissions</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html">Protecting
                  data using server-side encryption with Amazon Web Services
                  KMS</a> in the <i>Amazon S3 User Guide</i>.</p> </li> <li>
                  <p>If your Identity and Access Management (IAM) user or role
                  is in the same Amazon Web Services account as the KMS key,
                  then you must have these permissions on the key policy. If
                  your IAM user or role is in a different account from the key,
                  then you must have the permissions on both the key policy and
                  your IAM user or role.</p> </li> <li> <p>All <code>GET</code>
                  and <code>PUT</code> requests for an object protected by KMS
                  fail if you don't make them by using Secure Sockets Layer
                  (SSL), Transport Layer Security (TLS), or Signature Version 4.
                  For information about configuring any of the officially
                  supported Amazon Web Services SDKs and Amazon Web Services
                  CLI, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingAWSSDK.html#specify-signature-version">Specifying
                  the Signature Version in Request Authentication</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> </ul> </note> <p>For
                  more information about server-side encryption with KMS keys
                  (SSE-KMS), see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html">Protecting
                  Data Using Server-Side Encryption with KMS keys</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> <li> <p>Use
                  customer-provided encryption keys (SSE-C) – If you want to
                  manage your own encryption keys, provide all the following
                  headers in the request.</p> <ul> <li> <p>
                  <code>x-amz-server-side-encryption-customer-algorithm</code>
                  </p> </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key</code> </p>
                  </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key-MD5</code>
                  </p> </li> </ul> <p>For more information about server-side
                  encryption with customer-provided encryption keys (SSE-C), see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ServerSideEncryptionCustomerKeys.html">
                  Protecting data using server-side encryption with
                  customer-provided encryption keys (SSE-C)</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </li> </ul> </li> <li> <p> <b>Directory
                  buckets</b> -For directory buckets, only server-side
                  encryption with Amazon S3 managed keys (SSE-S3)
                  (<code>AES256</code>) is supported.</p> </li> </ul> </dd>
                  <dt>HTTP Host header syntax</dt> <dd> <p> <b>Directory buckets
                  </b> - The HTTP Host header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>CreateMultipartUpload</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListMultipartUploads.html">ListMultipartUploads</a>
                  </p> </li> </ul>
                tags:
                  - Create
                  - Multipart
                  - Uploads
                  - Bucket
                  - Keys
                  - '?uploads'
            /{Bucket}?session:
              GET:
                summary: CreateSession
                description: >-
                  <p>Creates a session that establishes temporary security
                  credentials to support fast authentication and authorization
                  for the Zonal endpoint APIs on directory buckets. For more
                  information about Zonal endpoint APIs that include the
                  Availability Zone in the request endpoint, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-APIs.html">S3
                  Express One Zone APIs</a> in the <i>Amazon S3 User Guide</i>.
                  </p> <p>To make Zonal endpoint API requests on a directory
                  bucket, use the <code>CreateSession</code> API operation.
                  Specifically, you grant <code>s3express:CreateSession</code>
                  permission to a bucket in a bucket policy or an IAM
                  identity-based policy. Then, you use IAM credentials to make
                  the <code>CreateSession</code> API request on the bucket,
                  which returns temporary security credentials that include the
                  access key ID, secret access key, session token, and
                  expiration. These credentials have associated permissions to
                  access the Zonal endpoint APIs. After the session is created,
                  you don’t need to use other policies to grant permissions to
                  each Zonal endpoint API individually. Instead, in your Zonal
                  endpoint API requests, you sign your requests by applying the
                  temporary security credentials of the session to the request
                  headers and following the SigV4 protocol for authentication.
                  You also apply the session token to the
                  <code>x-amz-s3session-token</code> request header for
                  authorization. Temporary security credentials are scoped to
                  the bucket and expire after 5 minutes. After the expiration
                  time, any calls that you make with those credentials will
                  fail. You must use IAM credentials again to make a
                  <code>CreateSession</code> API request that generates a new
                  set of temporary credentials for use. Temporary credentials
                  cannot be extended or refreshed beyond the original specified
                  interval.</p> <p>If you use Amazon Web Services SDKs, SDKs
                  handle the session token refreshes automatically to avoid
                  service interruptions when a session expires. We recommend
                  that you use the Amazon Web Services SDKs to initiate and
                  manage requests to the CreateSession API. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-optimizing-performance-guidelines-design-patterns.html#s3-express-optimizing-performance-session-authentication">Performance
                  guidelines and design patterns</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <ul> <li> <p>You must make requests for
                  this API operation to the Zonal endpoint. These endpoints
                  support virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.
                  Path-style requests are not supported. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b> <code>CopyObject</code> API
                  operation</b> - Unlike other Zonal endpoint APIs, the
                  <code>CopyObject</code> API operation doesn't use the
                  temporary security credentials returned from the
                  <code>CreateSession</code> API operation for authentication
                  and authorization. For information about authentication and
                  authorization of the <code>CopyObject</code> API operation on
                  directory buckets, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html">CopyObject</a>.</p>
                  </li> <li> <p> <b> <code>HeadBucket</code> API operation</b> -
                  Unlike other Zonal endpoint APIs, the <code>HeadBucket</code>
                  API operation doesn't use the temporary security credentials
                  returned from the <code>CreateSession</code> API operation for
                  authentication and authorization. For information about
                  authentication and authorization of the
                  <code>HeadBucket</code> API operation on directory buckets,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadBucket.html">HeadBucket</a>.</p>
                  </li> </ul> </note> <dl> <dt>Permissions</dt> <dd> <p>To
                  obtain temporary security credentials, you must create a
                  bucket policy or an IAM identity-based policy that grants
                  <code>s3express:CreateSession</code> permission to the bucket.
                  In a policy, you can have the
                  <code>s3express:SessionMode</code> condition key to control
                  who can create a <code>ReadWrite</code> or
                  <code>ReadOnly</code> session. For more information about
                  <code>ReadWrite</code> or <code>ReadOnly</code> sessions, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html#API_CreateSession_RequestParameters">
                  <code>x-amz-create-session-mode</code> </a>. For example
                  policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-example-bucket-policies.html">Example
                  bucket policies for S3 Express One Zone</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-identity-policies.html">Amazon
                  Web Services Identity and Access Management (IAM)
                  identity-based policies for S3 Express One Zone</a> in the
                  <i>Amazon S3 User Guide</i>. </p> <p>To grant cross-account
                  access to Zonal endpoint APIs, the bucket policy should also
                  grant both accounts the <code>s3express:CreateSession</code>
                  permission.</p> </dd> <dt>HTTP Host header syntax</dt> <dd>
                  <p> <b>Directory buckets </b> - The HTTP Host header syntax is
                  <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl>
                tags:
                  - Create
                  - Sessions
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
            /{Bucket}?analytics:
              PUT:
                summary: PutBucketAnalyticsConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets an analytics configuration for
                  the bucket (specified by the analytics configuration ID). You
                  can have up to 1,000 analytics configurations per bucket.</p>
                  <p>You can choose to have storage class analysis export
                  analysis reports sent to a comma-separated values (CSV) flat
                  file. See the <code>DataExport</code> request element. Reports
                  are updated daily and are based on the object filters that you
                  configure. When selecting data export, you specify a
                  destination bucket and an optional destination prefix where
                  the file is written. You can export the data to a destination
                  bucket in a different account. However, the destination bucket
                  must be in the same Region as the bucket that you are making
                  the PUT analytics configuration to. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/analytics-storage-class.html">Amazon
                  S3 Analytics – Storage Class Analysis</a>. </p> <important>
                  <p>You must create a bucket policy on the destination bucket
                  where the exported file is written to grant permissions to
                  Amazon S3 to write objects to the bucket. For an example
                  policy, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html#example-bucket-policies-use-case-9">Granting
                  Permissions for Amazon S3 Inventory and Storage Class
                  Analysis</a>.</p> </important> <p>To use this operation, you
                  must have permissions to perform the
                  <code>s3:PutAnalyticsConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>
                  <code>PutBucketAnalyticsConfiguration</code> has the following
                  special errors:</p> <ul> <li> <ul> <li> <p> <i>HTTP Error:
                  HTTP 400 Bad Request</i> </p> </li> <li> <p> <i>Code:
                  InvalidArgument</i> </p> </li> <li> <p> <i>Cause: Invalid
                  argument.</i> </p> </li> </ul> </li> <li> <ul> <li> <p>
                  <i>HTTP Error: HTTP 400 Bad Request</i> </p> </li> <li> <p>
                  <i>Code: TooManyConfigurations</i> </p> </li> <li> <p>
                  <i>Cause: You are attempting to create a new configuration but
                  have already reached the 1,000-configuration limit.</i> </p>
                  </li> </ul> </li> <li> <ul> <li> <p> <i>HTTP Error: HTTP 403
                  Forbidden</i> </p> </li> <li> <p> <i>Code: AccessDenied</i>
                  </p> </li> <li> <p> <i>Cause: You are not the owner of the
                  specified bucket, or you do not have the
                  s3:PutAnalyticsConfiguration bucket permission to set the
                  configuration on the bucket.</i> </p> </li> </ul> </li> </ul>
                  <p>The following operations are related to
                  <code>PutBucketAnalyticsConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAnalyticsConfiguration.html">GetBucketAnalyticsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketAnalyticsConfiguration.html">DeleteBucketAnalyticsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketAnalyticsConfigurations.html">ListBucketAnalyticsConfigurations</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Analytics
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
            /{Bucket}?cors:
              PUT:
                summary: PutBucketCors
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the <code>cors</code>
                  configuration for your bucket. If the configuration exists,
                  Amazon S3 replaces it.</p> <p>To use this operation, you must
                  be allowed to perform the <code>s3:PutBucketCORS</code>
                  action. By default, the bucket owner has this permission and
                  can grant it to others.</p> <p>You set this configuration on a
                  bucket so that the bucket can service cross-origin requests.
                  For example, you might want to enable a request whose origin
                  is <code>http://www.example.com</code> to access your Amazon
                  S3 bucket at <code>my.example.bucket.com</code> by using the
                  browser's <code>XMLHttpRequest</code> capability.</p> <p>To
                  enable cross-origin resource sharing (CORS) on a bucket, you
                  add the <code>cors</code> subresource to the bucket. The
                  <code>cors</code> subresource is an XML document in which you
                  configure rules that identify origins and the HTTP methods
                  that can be executed on your bucket. The document is limited
                  to 64 KB in size. </p> <p>When Amazon S3 receives a
                  cross-origin request (or a pre-flight OPTIONS request) against
                  a bucket, it evaluates the <code>cors</code> configuration on
                  the bucket and uses the first <code>CORSRule</code> rule that
                  matches the incoming browser request to enable a cross-origin
                  request. For a rule to match, the following conditions must be
                  met:</p> <ul> <li> <p>The request's <code>Origin</code> header
                  must match <code>AllowedOrigin</code> elements.</p> </li> <li>
                  <p>The request method (for example, GET, PUT, HEAD, and so on)
                  or the <code>Access-Control-Request-Method</code> header in
                  case of a pre-flight <code>OPTIONS</code> request must be one
                  of the <code>AllowedMethod</code> elements. </p> </li> <li>
                  <p>Every header specified in the
                  <code>Access-Control-Request-Headers</code> request header of
                  a pre-flight request must match an <code>AllowedHeader</code>
                  element. </p> </li> </ul> <p> For more information about CORS,
                  go to <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html">Enabling
                  Cross-Origin Resource Sharing</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following operations are related to
                  <code>PutBucketCors</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketCors.html">GetBucketCors</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketCors.html">DeleteBucketCors</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTOPTIONSobject.html">RESTOPTIONSobject</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - CORS
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
            /{Bucket}?encryption:
              PUT:
                summary: PutBucketEncryption
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>This action uses the
                  <code>encryption</code> subresource to configure default
                  encryption and Amazon S3 Bucket Keys for an existing
                  bucket.</p> <p>By default, all buckets have a default
                  encryption configuration that uses server-side encryption with
                  Amazon S3 managed keys (SSE-S3). You can optionally configure
                  default encryption for a bucket by using server-side
                  encryption with Key Management Service (KMS) keys (SSE-KMS) or
                  dual-layer server-side encryption with Amazon Web Services KMS
                  keys (DSSE-KMS). If you specify default encryption by using
                  SSE-KMS, you can also configure <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-key.html">Amazon
                  S3 Bucket Keys</a>. If you use PutBucketEncryption to set your
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html">default
                  bucket encryption</a> to SSE-KMS, you should verify that your
                  KMS key ID is correct. Amazon S3 does not validate the KMS key
                  ID provided in PutBucketEncryption requests.</p> <important>
                  <p>This action requires Amazon Web Services Signature Version
                  4. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">
                  Authenticating Requests (Amazon Web Services Signature Version
                  4)</a>. </p> </important> <p>To use this operation, you must
                  have permission to perform the
                  <code>s3:PutEncryptionConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a> in the
                  <i>Amazon S3 User Guide</i>. </p> <p>The following operations
                  are related to <code>PutBucketEncryption</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketEncryption.html">GetBucketEncryption</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketEncryption.html">DeleteBucketEncryption</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Encryption
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
            /{Bucket}?intelligent-tiering:
              PUT:
                summary: PutBucketIntelligentTieringConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Puts a S3 Intelligent-Tiering
                  configuration to the specified bucket. You can have up to
                  1,000 S3 Intelligent-Tiering configurations per bucket.</p>
                  <p>The S3 Intelligent-Tiering storage class is designed to
                  optimize storage costs by automatically moving data to the
                  most cost-effective storage access tier, without performance
                  impact or operational overhead. S3 Intelligent-Tiering
                  delivers automatic cost savings in three low latency and high
                  throughput access tiers. To get the lowest storage cost on
                  data that can be accessed in minutes to hours, you can choose
                  to activate additional archiving capabilities.</p> <p>The S3
                  Intelligent-Tiering storage class is the ideal storage class
                  for data with unknown, changing, or unpredictable access
                  patterns, independent of object size or retention period. If
                  the size of an object is less than 128 KB, it is not monitored
                  and not eligible for auto-tiering. Smaller objects can be
                  stored, but they are always charged at the Frequent Access
                  tier rates in the S3 Intelligent-Tiering storage class.</p>
                  <p>For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html#sc-dynamic-data-access">Storage
                  class for automatically optimizing frequently and infrequently
                  accessed objects</a>.</p> <p>Operations related to
                  <code>PutBucketIntelligentTieringConfiguration</code> include:
                  </p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketIntelligentTieringConfiguration.html">DeleteBucketIntelligentTieringConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketIntelligentTieringConfiguration.html">GetBucketIntelligentTieringConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketIntelligentTieringConfigurations.html">ListBucketIntelligentTieringConfigurations</a>
                  </p> </li> </ul> <note> <p>You only need S3
                  Intelligent-Tiering enabled on a bucket if you want to
                  automatically move objects stored in the S3
                  Intelligent-Tiering storage class to the Archive Access or
                  Deep Archive Access tier.</p> </note> <p>
                  <code>PutBucketIntelligentTieringConfiguration</code> has the
                  following special errors:</p> <dl> <dt>HTTP 400 Bad Request
                  Error</dt> <dd> <p> <i>Code:</i> InvalidArgument</p> <p>
                  <i>Cause:</i> Invalid Argument</p> </dd> <dt>HTTP 400 Bad
                  Request Error</dt> <dd> <p> <i>Code:</i>
                  TooManyConfigurations</p> <p> <i>Cause:</i> You are attempting
                  to create a new configuration but have already reached the
                  1,000-configuration limit. </p> </dd> <dt>HTTP 403 Forbidden
                  Error</dt> <dd> <p> <i>Cause:</i> You are not the owner of the
                  specified bucket, or you do not have the
                  <code>s3:PutIntelligentTieringConfiguration</code> bucket
                  permission to set the configuration on the bucket. </p> </dd>
                  </dl>
                tags:
                  - Put
                  - Bucket
                  - Intelligent
                  - Tiering
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
            /{Bucket}?inventory:
              PUT:
                summary: PutBucketInventoryConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>This implementation of the
                  <code>PUT</code> action adds an inventory configuration
                  (identified by the inventory ID) to the bucket. You can have
                  up to 1,000 inventory configurations per bucket. </p>
                  <p>Amazon S3 inventory generates inventories of the objects in
                  the bucket on a daily or weekly basis, and the results are
                  published to a flat file. The bucket that is inventoried is
                  called the <i>source</i> bucket, and the bucket where the
                  inventory flat file is stored is called the <i>destination</i>
                  bucket. The <i>destination</i> bucket must be in the same
                  Amazon Web Services Region as the <i>source</i> bucket. </p>
                  <p>When you configure an inventory for a <i>source</i> bucket,
                  you specify the <i>destination</i> bucket where you want the
                  inventory to be stored, and whether to generate the inventory
                  daily or weekly. You can also configure what object metadata
                  to include and whether to inventory all object versions or
                  only current versions. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-inventory.html">Amazon
                  S3 Inventory</a> in the Amazon S3 User Guide.</p> <important>
                  <p>You must create a bucket policy on the <i>destination</i>
                  bucket to grant permissions to Amazon S3 to write objects to
                  the bucket in the defined location. For an example policy, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html#example-bucket-policies-use-case-9">
                  Granting Permissions for Amazon S3 Inventory and Storage Class
                  Analysis</a>.</p> </important> <dl> <dt>Permissions</dt> <dd>
                  <p>To use this operation, you must have permission to perform
                  the <code>s3:PutInventoryConfiguration</code> action. The
                  bucket owner has this permission by default and can grant this
                  permission to others. </p> <p>The
                  <code>s3:PutInventoryConfiguration</code> permission allows a
                  user to create an <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-inventory.html">S3
                  Inventory</a> report that includes all object metadata fields
                  available and to specify the destination bucket to store the
                  inventory. A user with read access to objects in the
                  destination bucket can also access all object metadata fields
                  that are available in the inventory report. </p> <p>To
                  restrict access to an inventory report, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html#example-bucket-policies-use-case-10">Restricting
                  access to an Amazon S3 Inventory report</a> in the <i>Amazon
                  S3 User Guide</i>. For more information about the metadata
                  fields available in S3 Inventory, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-inventory.html#storage-inventory-contents">Amazon
                  S3 Inventory lists</a> in the <i>Amazon S3 User Guide</i>. For
                  more information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  related to bucket subresource operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Identity
                  and access management in Amazon S3</a> in the <i>Amazon S3
                  User Guide</i>.</p> </dd> </dl> <p>
                  <code>PutBucketInventoryConfiguration</code> has the following
                  special errors:</p> <dl> <dt>HTTP 400 Bad Request Error</dt>
                  <dd> <p> <i>Code:</i> InvalidArgument</p> <p> <i>Cause:</i>
                  Invalid Argument</p> </dd> <dt>HTTP 400 Bad Request Error</dt>
                  <dd> <p> <i>Code:</i> TooManyConfigurations</p> <p>
                  <i>Cause:</i> You are attempting to create a new configuration
                  but have already reached the 1,000-configuration limit. </p>
                  </dd> <dt>HTTP 403 Forbidden Error</dt> <dd> <p> <i>Cause:</i>
                  You are not the owner of the specified bucket, or you do not
                  have the <code>s3:PutInventoryConfiguration</code> bucket
                  permission to set the configuration on the bucket. </p> </dd>
                  </dl> <p>The following operations are related to
                  <code>PutBucketInventoryConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketInventoryConfiguration.html">GetBucketInventoryConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketInventoryConfiguration.html">DeleteBucketInventoryConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketInventoryConfigurations.html">ListBucketInventoryConfigurations</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Inventory
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
            /{Bucket}?lifecycle:
              PUT:
                summary: PutBucketLifecycleConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates a new lifecycle configuration
                  for the bucket or replaces an existing lifecycle
                  configuration. Keep in mind that this will overwrite an
                  existing lifecycle configuration, so if you want to retain any
                  configuration details, they must be included in the new
                  lifecycle configuration. For information about lifecycle
                  configuration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html">Managing
                  your storage lifecycle</a>.</p> <note> <p>Bucket lifecycle
                  configuration now supports specifying a lifecycle rule using
                  an object key name prefix, one or more object tags, or a
                  combination of both. Accordingly, this section describes the
                  latest API. The previous version of the API supported
                  filtering based only on an object key name prefix, which is
                  supported for backward compatibility. For the related API
                  description, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycle.html">PutBucketLifecycle</a>.</p>
                  </note> <dl> <dt>Rules</dt> <dd> <p>You specify the lifecycle
                  configuration in your request body. The lifecycle
                  configuration is specified as XML consisting of one or more
                  rules. An Amazon S3 Lifecycle configuration can have up to
                  1,000 rules. This limit is not adjustable. Each rule consists
                  of the following:</p> <ul> <li> <p>A filter identifying a
                  subset of objects to which the rule applies. The filter can be
                  based on a key name prefix, object tags, or a combination of
                  both.</p> </li> <li> <p>A status indicating whether the rule
                  is in effect.</p> </li> <li> <p>One or more lifecycle
                  transition and expiration actions that you want Amazon S3 to
                  perform on the objects identified by the filter. If the state
                  of your bucket is versioning-enabled or versioning-suspended,
                  you can have many versions of the same object (one current
                  version and zero or more noncurrent versions). Amazon S3
                  provides predefined actions that you can specify for current
                  and noncurrent object versions.</p> </li> </ul> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html">Object
                  Lifecycle Management</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/intro-lifecycle-rules.html">Lifecycle
                  Configuration Elements</a>.</p> </dd> <dt>Permissions</dt>
                  <dd> <p>By default, all Amazon S3 resources are private,
                  including buckets, objects, and related subresources (for
                  example, lifecycle configuration and website configuration).
                  Only the resource owner (that is, the Amazon Web Services
                  account that created it) can access the resource. The resource
                  owner can optionally grant access permissions to others by
                  writing an access policy. For this operation, a user must get
                  the <code>s3:PutLifecycleConfiguration</code> permission.</p>
                  <p>You can also explicitly deny permissions. An explicit deny
                  also supersedes any other permissions. If you want to block
                  users or accounts from removing or deleting objects from your
                  bucket, you must deny them permissions for the following
                  actions:</p> <ul> <li> <p> <code>s3:DeleteObject</code> </p>
                  </li> <li> <p> <code>s3:DeleteObjectVersion</code> </p> </li>
                  <li> <p> <code>s3:PutLifecycleConfiguration</code> </p> </li>
                  </ul> <p>For more information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> </dd>
                  </dl> <p>The following operations are related to
                  <code>PutBucketLifecycleConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-configuration-examples.html">Examples
                  of Lifecycle Configuration</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLifecycleConfiguration.html">GetBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketLifecycle.html">DeleteBucketLifecycle</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Lifecycle
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
            /{Bucket}?metrics:
              PUT:
                summary: PutBucketMetricsConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets a metrics configuration
                  (specified by the metrics configuration ID) for the bucket.
                  You can have up to 1,000 metrics configurations per bucket. If
                  you're updating an existing metrics configuration, note that
                  this is a full replacement of the existing metrics
                  configuration. If you don't include the elements you want to
                  keep, they are erased.</p> <p>To use this operation, you must
                  have permissions to perform the
                  <code>s3:PutMetricsConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>For
                  information about CloudWatch request metrics for Amazon S3,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/cloudwatch-monitoring.html">Monitoring
                  Metrics with Amazon CloudWatch</a>.</p> <p>The following
                  operations are related to
                  <code>PutBucketMetricsConfiguration</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketMetricsConfiguration.html">DeleteBucketMetricsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketMetricsConfiguration.html">GetBucketMetricsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketMetricsConfigurations.html">ListBucketMetricsConfigurations</a>
                  </p> </li> </ul> <p>
                  <code>PutBucketMetricsConfiguration</code> has the following
                  special error:</p> <ul> <li> <p>Error code:
                  <code>TooManyConfigurations</code> </p> <ul> <li>
                  <p>Description: You are attempting to create a new
                  configuration but have already reached the 1,000-configuration
                  limit.</p> </li> <li> <p>HTTP Status Code: HTTP 400 Bad
                  Request</p> </li> </ul> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Metrics
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
            /{Bucket}?ownershipControls:
              PUT:
                summary: PutBucketOwnershipControls
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or modifies
                  <code>OwnershipControls</code> for an Amazon S3 bucket. To use
                  this operation, you must have the
                  <code>s3:PutBucketOwnershipControls</code> permission. For
                  more information about Amazon S3 permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/user-guide/using-with-s3-actions.html">Specifying
                  permissions in a policy</a>. </p> <p>For information about
                  Amazon S3 Object Ownership, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/user-guide/about-object-ownership.html">Using
                  object ownership</a>. </p> <p>The following operations are
                  related to <code>PutBucketOwnershipControls</code>:</p> <ul>
                  <li> <p> <a>GetBucketOwnershipControls</a> </p> </li> <li> <p>
                  <a>DeleteBucketOwnershipControls</a> </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Ownership
                  - Controls
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
            /{Bucket}?policy:
              PUT:
                summary: PutBucketPolicy
                description: >-
                  <p>Applies an Amazon S3 bucket policy to an Amazon S3
                  bucket.</p> <note> <p> <b>Directory buckets </b> - For
                  directory buckets, you must make requests for this API
                  operation to the Regional endpoint. These endpoints support
                  path-style requests in the format
                  <code>https://s3express-control.<i>region_code</i>.amazonaws.com/<i>bucket-name</i>
                  </code>. Virtual-hosted-style requests aren't supported. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <p>If
                  you are using an identity other than the root user of the
                  Amazon Web Services account that owns the bucket, the calling
                  identity must both have the <code>PutBucketPolicy</code>
                  permissions on the specified bucket and belong to the bucket
                  owner's account in order to use this operation.</p> <p>If you
                  don't have <code>PutBucketPolicy</code> permissions, Amazon S3
                  returns a <code>403 Access Denied</code> error. If you have
                  the correct permissions, but you're not using an identity that
                  belongs to the bucket owner's account, Amazon S3 returns a
                  <code>405 Method Not Allowed</code> error.</p> <important>
                  <p>To ensure that bucket owners don't inadvertently lock
                  themselves out of their own buckets, the root principal in a
                  bucket owner's Amazon Web Services account can perform the
                  <code>GetBucketPolicy</code>, <code>PutBucketPolicy</code>,
                  and <code>DeleteBucketPolicy</code> API actions, even if their
                  bucket policy explicitly denies the root principal's access.
                  Bucket owner root principals can only be blocked from
                  performing these API actions by VPC endpoint policies and
                  Amazon Web Services Organizations policies.</p> </important>
                  <ul> <li> <p> <b>General purpose bucket permissions</b> - The
                  <code>s3:PutBucketPolicy</code> permission is required in a
                  policy. For more information about general purpose buckets
                  bucket policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-iam-policies.html">Using
                  Bucket Policies and User Policies</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b>Directory bucket
                  permissions</b> - To grant access to this API operation, you
                  must have the <code>s3express:PutBucketPolicy</code>
                  permission in an IAM identity-based policy instead of a bucket
                  policy. Cross-account access to this API operation isn't
                  supported. This operation can only be performed by the Amazon
                  Web Services account that owns the resource. For more
                  information about directory bucket policies and permissions,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam.html">Amazon
                  Web Services Identity and Access Management (IAM) for S3
                  Express One Zone</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </li> </ul> </dd> <dt>Example bucket policies</dt> <dd> <p>
                  <b>General purpose buckets example bucket policies</b> - See
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html">Bucket
                  policy examples</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p> <b>Directory bucket example bucket policies</b> - See <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-example-bucket-policies.html">Example
                  bucket policies for S3 Express One Zone</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </dd> <dt>HTTP Host header syntax</dt>
                  <dd> <p> <b>Directory buckets </b> - The HTTP Host header
                  syntax is
                  <code>s3express-control.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>PutBucketPolicy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Policies
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
            /{Bucket}?replication:
              PUT:
                summary: PutBucketReplication
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p> Creates a replication configuration
                  or replaces an existing one. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html">Replication</a>
                  in the <i>Amazon S3 User Guide</i>. </p> <p>Specify the
                  replication configuration in the request body. In the
                  replication configuration, you provide the name of the
                  destination bucket or buckets where you want Amazon S3 to
                  replicate objects, the IAM role that Amazon S3 can assume to
                  replicate objects on your behalf, and other relevant
                  information. You can invoke this request for a specific Amazon
                  Web Services Region by using the <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-requestedregion">
                  <code>aws:RequestedRegion</code> </a> condition key.</p> <p>A
                  replication configuration must include at least one rule, and
                  can contain a maximum of 1,000. Each rule identifies a subset
                  of objects to replicate by filtering the objects in the source
                  bucket. To choose additional subsets of objects to replicate,
                  add a rule for each subset.</p> <p>To specify a subset of the
                  objects in the source bucket to apply a replication rule to,
                  add the Filter element as a child of the Rule element. You can
                  filter objects based on an object key prefix, one or more
                  object tags, or both. When you add the Filter element in the
                  configuration, you must also add the following elements:
                  <code>DeleteMarkerReplication</code>, <code>Status</code>, and
                  <code>Priority</code>.</p> <note> <p>If you are using an
                  earlier version of the replication configuration, Amazon S3
                  handles replication of delete markers differently. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-backward-compat-considerations">Backward
                  Compatibility</a>.</p> </note> <p>For information about
                  enabling versioning on a bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html">Using
                  Versioning</a>.</p> <dl> <dt>Handling Replication of Encrypted
                  Objects</dt> <dd> <p>By default, Amazon S3 doesn't replicate
                  objects that are stored at rest using server-side encryption
                  with KMS keys. To replicate Amazon Web Services KMS-encrypted
                  objects, add the following:
                  <code>SourceSelectionCriteria</code>,
                  <code>SseKmsEncryptedObjects</code>, <code>Status</code>,
                  <code>EncryptionConfiguration</code>, and
                  <code>ReplicaKmsKeyID</code>. For information about
                  replication configuration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-config-for-kms-objects.html">Replicating
                  Objects Created with SSE Using KMS keys</a>.</p> <p>For
                  information on <code>PutBucketReplication</code> errors, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#ReplicationErrorCodeList">List
                  of replication-related error codes</a> </p> </dd>
                  <dt>Permissions</dt> <dd> <p>To create a
                  <code>PutBucketReplication</code> request, you must have
                  <code>s3:PutReplicationConfiguration</code> permissions for
                  the bucket. </p> <p>By default, a resource owner, in this case
                  the Amazon Web Services account that created the bucket, can
                  perform this operation. The resource owner can also grant
                  others permissions to perform the operation. For more
                  information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <note>
                  <p>To perform this operation, the user or role performing the
                  action must have the <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html">iam:PassRole</a>
                  permission.</p> </note> </dd> </dl> <p>The following
                  operations are related to
                  <code>PutBucketReplication</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketReplication.html">GetBucketReplication</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketReplication.html">DeleteBucketReplication</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Replication
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
            /{Bucket}?tagging:
              PUT:
                summary: PutBucketTagging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the tags for a bucket.</p> <p>Use
                  tags to organize your Amazon Web Services bill to reflect your
                  own cost structure. To do this, sign up to get your Amazon Web
                  Services account bill with tag key values included. Then, to
                  see the cost of combined resources, organize your billing
                  information according to resources with the same tag key
                  values. For example, you can tag several resources with a
                  specific application name, and then organize your billing
                  information to see the total cost of that application across
                  several services. For more information, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Cost
                  Allocation and Tagging</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html">Using
                  Cost Allocation in Amazon S3 Bucket Tags</a>.</p> <note> <p>
                  When this operation sets the tags for a bucket, it will
                  overwrite any current tags the bucket already has. You cannot
                  use this operation to add tags to an existing list of
                  tags.</p> </note> <p>To use this operation, you must have
                  permissions to perform the <code>s3:PutBucketTagging</code>
                  action. The bucket owner has this permission by default and
                  can grant this permission to others. For more information
                  about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>
                  <code>PutBucketTagging</code> has the following special
                  errors. For more Amazon S3 errors see, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html">Error
                  Responses</a>.</p> <ul> <li> <p> <code>InvalidTag</code> - The
                  tag provided was not a valid tag. This error can occur if the
                  tag did not pass input validation. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html">Using
                  Cost Allocation in Amazon S3 Bucket Tags</a>.</p> </li> <li>
                  <p> <code>MalformedXML</code> - The XML provided does not
                  match the schema.</p> </li> <li> <p>
                  <code>OperationAborted</code> - A conflicting conditional
                  action is currently in progress against this resource. Please
                  try again.</p> </li> <li> <p> <code>InternalError</code> - The
                  service was unable to apply the provided tag to the
                  bucket.</p> </li> </ul> <p>The following operations are
                  related to <code>PutBucketTagging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketTagging.html">GetBucketTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketTagging.html">DeleteBucketTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Tagging
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
            /{Bucket}?website:
              PUT:
                summary: PutBucketWebsite
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the configuration of the website
                  that is specified in the <code>website</code> subresource. To
                  configure a bucket as a website, you can add this subresource
                  on the bucket with website configuration information such as
                  the file name of the index document and any redirect rules.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html">Hosting
                  Websites on Amazon S3</a>.</p> <p>This PUT action requires the
                  <code>S3:PutBucketWebsite</code> permission. By default, only
                  the bucket owner can configure the website attached to a
                  bucket; however, bucket owners can allow other users to set
                  the website configuration by writing a bucket policy that
                  grants them the <code>S3:PutBucketWebsite</code>
                  permission.</p> <p>To redirect all website requests sent to
                  the bucket's website endpoint, you add a website configuration
                  with the following elements. Because all requests are sent to
                  another website, you don't need to provide index document name
                  for the bucket.</p> <ul> <li> <p>
                  <code>WebsiteConfiguration</code> </p> </li> <li> <p>
                  <code>RedirectAllRequestsTo</code> </p> </li> <li> <p>
                  <code>HostName</code> </p> </li> <li> <p>
                  <code>Protocol</code> </p> </li> </ul> <p>If you want granular
                  control over redirects, you can use the following elements to
                  add routing rules that describe conditions for redirecting
                  requests and information about the redirect destination. In
                  this case, the website configuration must provide an index
                  document for the bucket, because some requests might not be
                  redirected. </p> <ul> <li> <p>
                  <code>WebsiteConfiguration</code> </p> </li> <li> <p>
                  <code>IndexDocument</code> </p> </li> <li> <p>
                  <code>Suffix</code> </p> </li> <li> <p>
                  <code>ErrorDocument</code> </p> </li> <li> <p>
                  <code>Key</code> </p> </li> <li> <p> <code>RoutingRules</code>
                  </p> </li> <li> <p> <code>RoutingRule</code> </p> </li> <li>
                  <p> <code>Condition</code> </p> </li> <li> <p>
                  <code>HttpErrorCodeReturnedEquals</code> </p> </li> <li> <p>
                  <code>KeyPrefixEquals</code> </p> </li> <li> <p>
                  <code>Redirect</code> </p> </li> <li> <p>
                  <code>Protocol</code> </p> </li> <li> <p>
                  <code>HostName</code> </p> </li> <li> <p>
                  <code>ReplaceKeyPrefixWith</code> </p> </li> <li> <p>
                  <code>ReplaceKeyWith</code> </p> </li> <li> <p>
                  <code>HttpRedirectCode</code> </p> </li> </ul> <p>Amazon S3
                  has a limitation of 50 routing rules per website
                  configuration. If you require more than 50 routing rules, you
                  can use object redirect. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/how-to-page-redirect.html">Configuring
                  an Object Redirect</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p>The maximum request length is limited to 128 KB.</p>
                tags:
                  - Put
                  - Bucket
                  - Websites
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
            /{Bucket}/{Key+}?tagging:
              PUT:
                summary: PutObjectTagging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the supplied tag-set to an object
                  that already exists in a bucket. A tag is a key-value pair.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-tagging.html">Object
                  Tagging</a>.</p> <p>You can associate tags with an object by
                  sending a PUT request against the tagging subresource that is
                  associated with the object. You can retrieve tags by sending a
                  GET request. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html">GetObjectTagging</a>.</p>
                  <p>For tagging-related restrictions related to characters and
                  encodings, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/allocation-tag-restrictions.html">Tag
                  Restrictions</a>. Note that Amazon S3 limits the maximum
                  number of tags to 10 tags per object.</p> <p>To use this
                  operation, you must have permission to perform the
                  <code>s3:PutObjectTagging</code> action. By default, the
                  bucket owner has this permission and can grant this permission
                  to others.</p> <p>To put tags of any other version, use the
                  <code>versionId</code> query parameter. You also need
                  permission for the <code>s3:PutObjectVersionTagging</code>
                  action.</p> <p> <code>PutObjectTagging</code> has the
                  following special errors. For more Amazon S3 errors see, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html">Error
                  Responses</a>.</p> <ul> <li> <p> <code>InvalidTag</code> - The
                  tag provided was not a valid tag. This error can occur if the
                  tag did not pass input validation. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-tagging.html">Object
                  Tagging</a>.</p> </li> <li> <p> <code>MalformedXML</code> -
                  The XML provided does not match the schema.</p> </li> <li> <p>
                  <code>OperationAborted</code> - A conflicting conditional
                  action is currently in progress against this resource. Please
                  try again.</p> </li> <li> <p> <code>InternalError</code> - The
                  service was unable to apply the provided tag to the
                  object.</p> </li> </ul> <p>The following operations are
                  related to <code>PutObjectTagging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html">GetObjectTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObjectTagging.html">DeleteObjectTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Objects
                  - Tagging
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
            /{Bucket}?delete:
              POST:
                summary: DeleteObjects
                description: >-
                  <p>This operation enables you to delete multiple objects from
                  a bucket using a single HTTP request. If you know the object
                  keys that you want to delete, then this operation provides a
                  suitable alternative to sending individual delete requests,
                  reducing per-request overhead.</p> <p>The request can contain
                  a list of up to 1000 keys that you want to delete. In the XML,
                  you provide the object key names, and optionally, version IDs
                  if you want to delete a specific version of the object from a
                  versioning-enabled bucket. For each key, Amazon S3 performs a
                  delete operation and returns the result of that delete,
                  success or failure, in the response. Note that if the object
                  specified in the request is not found, Amazon S3 returns the
                  result as deleted.</p> <note> <ul> <li> <p> <b>Directory
                  buckets</b> - S3 Versioning isn't enabled and supported for
                  directory buckets.</p> </li> <li> <p> <b>Directory buckets</b>
                  - For directory buckets, you must make requests for this API
                  operation to the Zonal endpoint. These endpoints support
                  virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> </ul> </note> <p>The operation supports
                  two modes for the response: verbose and quiet. By default, the
                  operation uses verbose mode in which the response includes the
                  result of deletion of each key in your request. In quiet mode
                  the response includes only keys where the delete operation
                  encountered an error. For a successful deletion in a quiet
                  mode, the operation does not return any information about the
                  delete in the response body.</p> <p>When performing this
                  action on an MFA Delete enabled bucket, that attempts to
                  delete any versioned objects, you must include an MFA token.
                  If you do not provide one, the entire request will fail, even
                  if there are non-versioned objects you are trying to delete.
                  If you provide an invalid token, whether there are versioned
                  keys in the request or not, the entire Multi-Object Delete
                  request will fail. For information about MFA Delete, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html#MultiFactorAuthenticationDelete">MFA
                  Delete</a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>
                  <b>Directory buckets</b> - MFA delete is not supported by
                  directory buckets.</p> </note> <dl> <dt>Permissions</dt> <dd>
                  <ul> <li> <p> <b>General purpose bucket permissions</b> - The
                  following permissions are required in your policies when your
                  <code>DeleteObjects</code> request includes specific
                  headers.</p> <ul> <li> <p> <b> <code>s3:DeleteObject</code>
                  </b> - To delete an object from a bucket, you must always
                  specify the <code>s3:DeleteObject</code> permission.</p> </li>
                  <li> <p> <b> <code>s3:DeleteObjectVersion</code> </b> - To
                  delete a specific version of an object from a versiong-enabled
                  bucket, you must specify the
                  <code>s3:DeleteObjectVersion</code> permission.</p> </li>
                  </ul> </li> <li> <p> <b>Directory bucket permissions</b> - To
                  grant access to this API operation on a directory bucket, we
                  recommend that you use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Content-MD5 request header</dt> <dd> <ul> <li> <p>
                  <b>General purpose bucket</b> - The Content-MD5 request header
                  is required for all Multi-Object Delete requests. Amazon S3
                  uses the header value to ensure that your request body has not
                  been altered in transit.</p> </li> <li> <p> <b>Directory
                  bucket</b> - The Content-MD5 request header or a additional
                  checksum request header (including
                  <code>x-amz-checksum-crc32</code>,
                  <code>x-amz-checksum-crc32c</code>,
                  <code>x-amz-checksum-sha1</code>, or
                  <code>x-amz-checksum-sha256</code>) is required for all
                  Multi-Object Delete requests.</p> </li> </ul> </dd> <dt>HTTP
                  Host header syntax</dt> <dd> <p> <b>Directory buckets </b> -
                  The HTTP Host header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>DeleteObjects</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateMultipartUpload.html">CreateMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> </ul>
                tags:
                  - Delete
                  - Objects
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
            /{Bucket}?publicAccessBlock:
              PUT:
                summary: PutPublicAccessBlock
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or modifies the
                  <code>PublicAccessBlock</code> configuration for an Amazon S3
                  bucket. To use this operation, you must have the
                  <code>s3:PutBucketPublicAccessBlock</code> permission. For
                  more information about Amazon S3 permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a>.</p> <important> <p>When Amazon S3
                  evaluates the <code>PublicAccessBlock</code> configuration for
                  a bucket or an object, it checks the
                  <code>PublicAccessBlock</code> configuration for both the
                  bucket (or the bucket that contains the object) and the bucket
                  owner's account. If the <code>PublicAccessBlock</code>
                  configurations are different between the bucket and the
                  account, Amazon S3 uses the most restrictive combination of
                  the bucket-level and account-level settings.</p> </important>
                  <p>For more information about when Amazon S3 considers a
                  bucket or an object public, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status">The
                  Meaning of "Public"</a>.</p> <p>The following operations are
                  related to <code>PutPublicAccessBlock</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetPublicAccessBlock.html">GetPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeletePublicAccessBlock.html">DeletePublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketPolicyStatus.html">GetBucketPolicyStatus</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html">Using
                  Amazon S3 Block Public Access</a> </p> </li> </ul>
                tags:
                  - Put
                  - Public
                  - Access
                  - Blocks
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
            /{Bucket}?accelerate:
              PUT:
                summary: PutBucketAccelerateConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the accelerate configuration of
                  an existing bucket. Amazon S3 Transfer Acceleration is a
                  bucket-level feature that enables you to perform faster data
                  transfers to Amazon S3.</p> <p> To use this operation, you
                  must have permission to perform the
                  <code>s3:PutAccelerateConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>
                  The Transfer Acceleration state of a bucket can be set to one
                  of the following two values:</p> <ul> <li> <p> Enabled –
                  Enables accelerated data transfers to the bucket.</p> </li>
                  <li> <p> Suspended – Disables accelerated data transfers to
                  the bucket.</p> </li> </ul> <p>The <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAccelerateConfiguration.html">GetBucketAccelerateConfiguration</a>
                  action returns the transfer acceleration state of a
                  bucket.</p> <p>After setting the Transfer Acceleration state
                  of a bucket to Enabled, it might take up to thirty minutes
                  before the data transfer rates to the bucket increase.</p> <p>
                  The name of the bucket used for Transfer Acceleration must be
                  DNS-compliant and must not contain periods (".").</p> <p> For
                  more information about transfer acceleration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html">Transfer
                  Acceleration</a>.</p> <p>The following operations are related
                  to <code>PutBucketAccelerateConfiguration</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAccelerateConfiguration.html">GetBucketAccelerateConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Accelerate
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
            /{Bucket}?acl:
              PUT:
                summary: PutBucketAcl
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the permissions on an existing
                  bucket using access control lists (ACL). For more information,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/S3_ACLs_UsingACLs.html">Using
                  ACLs</a>. To set the ACL of a bucket, you must have the
                  <code>WRITE_ACP</code> permission.</p> <p>You can use one of
                  the following two ways to set a bucket's permissions:</p> <ul>
                  <li> <p>Specify the ACL in the request body</p> </li> <li>
                  <p>Specify permissions using request headers</p> </li> </ul>
                  <note> <p>You cannot specify access permission using both the
                  body and the request headers.</p> </note> <p>Depending on your
                  application needs, you may choose to set the ACL on a bucket
                  using either the request body or the headers. For example, if
                  you have an existing application that updates a bucket ACL
                  using the request body, then you can continue to use that
                  approach.</p> <important> <p>If your bucket uses the bucket
                  owner enforced setting for S3 Object Ownership, ACLs are
                  disabled and no longer affect permissions. You must use
                  policies to grant access to your bucket and the objects in it.
                  Requests to set ACLs or update ACLs fail and return the
                  <code>AccessControlListNotSupported</code> error code.
                  Requests to read ACLs are still supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html">Controlling
                  object ownership</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </important> <dl> <dt>Permissions</dt> <dd> <p>You can set
                  access permissions by using one of the following methods:</p>
                  <ul> <li> <p>Specify a canned ACL with the
                  <code>x-amz-acl</code> request header. Amazon S3 supports a
                  set of predefined ACLs, known as <i>canned ACLs</i>. Each
                  canned ACL has a predefined set of grantees and permissions.
                  Specify the canned ACL name as the value of
                  <code>x-amz-acl</code>. If you use this header, you cannot use
                  other access control-specific headers in your request. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#CannedACL">Canned
                  ACL</a>.</p> </li> <li> <p>Specify access permissions
                  explicitly with the <code>x-amz-grant-read</code>,
                  <code>x-amz-grant-read-acp</code>,
                  <code>x-amz-grant-write-acp</code>, and
                  <code>x-amz-grant-full-control</code> headers. When using
                  these headers, you specify explicit access permissions and
                  grantees (Amazon Web Services accounts or Amazon S3 groups)
                  who will receive the permission. If you use these ACL-specific
                  headers, you cannot use the <code>x-amz-acl</code> header to
                  set a canned ACL. These parameters map to the set of
                  permissions that Amazon S3 supports in an ACL. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html">Access
                  Control List (ACL) Overview</a>.</p> <p>You specify each
                  grantee as a type=value pair, where the type is one of the
                  following:</p> <ul> <li> <p> <code>id</code> – if the value
                  specified is the canonical user ID of an Amazon Web Services
                  account</p> </li> <li> <p> <code>uri</code> – if you are
                  granting permissions to a predefined group</p> </li> <li> <p>
                  <code>emailAddress</code> – if the value specified is the
                  email address of an Amazon Web Services account</p> <note>
                  <p>Using email addresses to specify a grantee is only
                  supported in the following Amazon Web Services Regions: </p>
                  <ul> <li> <p>US East (N. Virginia)</p> </li> <li> <p>US West
                  (N. California)</p> </li> <li> <p> US West (Oregon)</p> </li>
                  <li> <p> Asia Pacific (Singapore)</p> </li> <li> <p>Asia
                  Pacific (Sydney)</p> </li> <li> <p>Asia Pacific (Tokyo)</p>
                  </li> <li> <p>Europe (Ireland)</p> </li> <li> <p>South America
                  (São Paulo)</p> </li> </ul> <p>For a list of all the Amazon S3
                  supported Regions and endpoints, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> <p>For example, the
                  following <code>x-amz-grant-write</code> header grants create,
                  overwrite, and delete objects permission to LogDelivery group
                  predefined by Amazon S3 and two Amazon Web Services accounts
                  identified by their email addresses.</p> <p>
                  <code>x-amz-grant-write:
                  uri="http://acs.amazonaws.com/groups/s3/LogDelivery",
                  id="111122223333", id="555566667777" </code> </p> </li> </ul>
                  <p>You can use either a canned ACL or specify access
                  permissions explicitly. You cannot do both.</p> </dd>
                  <dt>Grantee Values</dt> <dd> <p>You can specify the person
                  (grantee) to whom you're assigning access rights (using
                  request elements) in the following ways:</p> <ul> <li> <p>By
                  the person's ID:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="CanonicalUser"&gt;&lt;ID&gt;&lt;&gt;ID&lt;&gt;&lt;/ID&gt;&lt;DisplayName&gt;&lt;&gt;GranteesEmail&lt;&gt;&lt;/DisplayName&gt;
                  &lt;/Grantee&gt;</code> </p> <p>DisplayName is optional and
                  ignored in the request</p> </li> <li> <p>By URI:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="Group"&gt;&lt;URI&gt;&lt;&gt;http://acs.amazonaws.com/groups/global/AuthenticatedUsers&lt;&gt;&lt;/URI&gt;&lt;/Grantee&gt;</code>
                  </p> </li> <li> <p>By Email address:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="AmazonCustomerByEmail"&gt;&lt;EmailAddress&gt;&lt;&gt;Grantees@email.com&lt;&gt;&lt;/EmailAddress&gt;&amp;&lt;/Grantee&gt;</code>
                  </p> <p>The grantee is resolved to the CanonicalUser and, in a
                  response to a GET Object acl request, appears as the
                  CanonicalUser. </p> <note> <p>Using email addresses to specify
                  a grantee is only supported in the following Amazon Web
                  Services Regions: </p> <ul> <li> <p>US East (N. Virginia)</p>
                  </li> <li> <p>US West (N. California)</p> </li> <li> <p> US
                  West (Oregon)</p> </li> <li> <p> Asia Pacific (Singapore)</p>
                  </li> <li> <p>Asia Pacific (Sydney)</p> </li> <li> <p>Asia
                  Pacific (Tokyo)</p> </li> <li> <p>Europe (Ireland)</p> </li>
                  <li> <p>South America (São Paulo)</p> </li> </ul> <p>For a
                  list of all the Amazon S3 supported Regions and endpoints, see
                  <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> </dd> </dl> <p>The
                  following operations are related to
                  <code>PutBucketAcl</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectAcl.html">GetObjectAcl</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - ACL
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
            /{Bucket}?location:
              GET:
                summary: GetBucketLocation
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns the Region the bucket resides
                  in. You set the bucket's Region using the
                  <code>LocationConstraint</code> request parameter in a
                  <code>CreateBucket</code> request. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>.</p>
                  <p>When you use this API operation with an access point,
                  provide the alias of the access point in place of the bucket
                  name.</p> <p>When you use this API operation with an Object
                  Lambda access point, provide the alias of the Object Lambda
                  access point in place of the bucket name. If the Object Lambda
                  access point alias in a request is not valid, the error code
                  <code>InvalidAccessPointAliasError</code> is returned. For
                  more information about
                  <code>InvalidAccessPointAliasError</code>, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#ErrorCodeList">List
                  of Error Codes</a>.</p> <note> <p>We recommend that you use <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadBucket.html">HeadBucket</a>
                  to return the Region that a bucket resides in. For backward
                  compatibility, Amazon S3 continues to support
                  GetBucketLocation.</p> </note> <p>The following operations are
                  related to <code>GetBucketLocation</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Bucket
                  - Locations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
            /{Bucket}?logging:
              PUT:
                summary: PutBucketLogging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Set the logging parameters for a
                  bucket and to specify permissions for who can view and modify
                  the logging parameters. All logs are saved to buckets in the
                  same Amazon Web Services Region as the source bucket. To set
                  the logging status of a bucket, you must be the bucket
                  owner.</p> <p>The bucket owner is automatically granted
                  FULL_CONTROL to all logs. You use the <code>Grantee</code>
                  request element to grant access to other people. The
                  <code>Permissions</code> request element specifies the kind of
                  access the grantee has to the logs.</p> <important> <p>If the
                  target bucket for log delivery uses the bucket owner enforced
                  setting for S3 Object Ownership, you can't use the
                  <code>Grantee</code> request element to grant access to
                  others. Permissions can only be granted using policies. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/enable-server-access-logging.html#grant-log-delivery-permissions-general">Permissions
                  for server access log delivery</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </important> <dl> <dt>Grantee Values</dt> <dd>
                  <p>You can specify the person (grantee) to whom you're
                  assigning access rights (by using request elements) in the
                  following ways:</p> <ul> <li> <p>By the person's ID:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="CanonicalUser"&gt;&lt;ID&gt;&lt;&gt;ID&lt;&gt;&lt;/ID&gt;&lt;DisplayName&gt;&lt;&gt;GranteesEmail&lt;&gt;&lt;/DisplayName&gt;
                  &lt;/Grantee&gt;</code> </p> <p> <code>DisplayName</code> is
                  optional and ignored in the request.</p> </li> <li> <p>By
                  Email address:</p> <p> <code> &lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="AmazonCustomerByEmail"&gt;&lt;EmailAddress&gt;&lt;&gt;Grantees@email.com&lt;&gt;&lt;/EmailAddress&gt;&lt;/Grantee&gt;</code>
                  </p> <p>The grantee is resolved to the
                  <code>CanonicalUser</code> and, in a response to a
                  <code>GETObjectAcl</code> request, appears as the
                  CanonicalUser.</p> </li> <li> <p>By URI:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="Group"&gt;&lt;URI&gt;&lt;&gt;http://acs.amazonaws.com/groups/global/AuthenticatedUsers&lt;&gt;&lt;/URI&gt;&lt;/Grantee&gt;</code>
                  </p> </li> </ul> </dd> </dl> <p>To enable logging, you use
                  <code>LoggingEnabled</code> and its children request elements.
                  To disable logging, you use an empty
                  <code>BucketLoggingStatus</code> request element:</p> <p>
                  <code>&lt;BucketLoggingStatus
                  xmlns="http://doc.s3.amazonaws.com/2006-03-01" /&gt;</code>
                  </p> <p>For more information about server access logging, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ServerLogs.html">Server
                  Access Logging</a> in the <i>Amazon S3 User Guide</i>. </p>
                  <p>For more information about creating a bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>.
                  For more information about returning the logging status of a
                  bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLogging.html">GetBucketLogging</a>.</p>
                  <p>The following operations are related to
                  <code>PutBucketLogging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLogging.html">GetBucketLogging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Logging
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
            /{Bucket}?notification:
              PUT:
                summary: PutBucketNotificationConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Enables notifications of specified
                  events for a bucket. For more information about event
                  notifications, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html">Configuring
                  Event Notifications</a>.</p> <p>Using this API, you can
                  replace an existing notification configuration. The
                  configuration is an XML file that defines the event types that
                  you want Amazon S3 to publish and the destination where you
                  want Amazon S3 to publish an event notification when it
                  detects an event of the specified type.</p> <p>By default,
                  your bucket has no event notifications configured. That is,
                  the notification configuration will be an empty
                  <code>NotificationConfiguration</code>.</p> <p>
                  <code>&lt;NotificationConfiguration&gt;</code> </p> <p>
                  <code>&lt;/NotificationConfiguration&gt;</code> </p> <p>This
                  action replaces the existing notification configuration with
                  the configuration you include in the request body.</p>
                  <p>After Amazon S3 receives this request, it first verifies
                  that any Amazon Simple Notification Service (Amazon SNS) or
                  Amazon Simple Queue Service (Amazon SQS) destination exists,
                  and that the bucket owner has permission to publish to it by
                  sending a test notification. In the case of Lambda
                  destinations, Amazon S3 verifies that the Lambda function
                  permissions grant Amazon S3 permission to invoke the function
                  from the Amazon S3 bucket. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html">Configuring
                  Notifications for Amazon S3 Events</a>.</p> <p>You can disable
                  notifications by adding the empty NotificationConfiguration
                  element.</p> <p>For more information about the number of event
                  notification configurations that you can create per bucket,
                  see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/s3.html#limits_s3">Amazon
                  S3 service quotas</a> in <i>Amazon Web Services General
                  Reference</i>.</p> <p>By default, only the bucket owner can
                  configure notifications on a bucket. However, bucket owners
                  can use a bucket policy to grant permission to other users to
                  set this configuration with the required
                  <code>s3:PutBucketNotification</code> permission.</p> <note>
                  <p>The PUT notification is an atomic operation. For example,
                  suppose your notification configuration includes SNS topic,
                  SQS queue, and Lambda function configurations. When you send a
                  PUT request with this configuration, Amazon S3 sends test
                  messages to your SNS topic. If the message fails, the entire
                  PUT action will fail, and Amazon S3 will not add the
                  configuration to your bucket.</p> </note> <p>If the
                  configuration in the request body includes only one
                  <code>TopicConfiguration</code> specifying only the
                  <code>s3:ReducedRedundancyLostObject</code> event type, the
                  response will also include the
                  <code>x-amz-sns-test-message-id</code> header containing the
                  message ID of the test notification sent to the topic.</p>
                  <p>The following action is related to
                  <code>PutBucketNotificationConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketNotificationConfiguration.html">GetBucketNotificationConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Notifications
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
            /{Bucket}?policyStatus:
              GET:
                summary: GetBucketPolicyStatus
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Retrieves the policy status for an
                  Amazon S3 bucket, indicating whether the bucket is public. In
                  order to use this operation, you must have the
                  <code>s3:GetBucketPolicyStatus</code> permission. For more
                  information about Amazon S3 permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a>.</p> <p> For more information
                  about when Amazon S3 considers a bucket public, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status">The
                  Meaning of "Public"</a>. </p> <p>The following operations are
                  related to <code>GetBucketPolicyStatus</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html">Using
                  Amazon S3 Block Public Access</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetPublicAccessBlock.html">GetPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutPublicAccessBlock.html">PutPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeletePublicAccessBlock.html">DeletePublicAccessBlock</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Bucket
                  - Policies
                  - Status
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
            /{Bucket}?requestPayment:
              PUT:
                summary: PutBucketRequestPayment
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the request payment configuration
                  for a bucket. By default, the bucket owner pays for downloads
                  from the bucket. This configuration parameter enables the
                  bucket owner (only) to specify that the person requesting the
                  download will be charged for the download. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RequesterPaysBuckets.html">Requester
                  Pays Buckets</a>.</p> <p>The following operations are related
                  to <code>PutBucketRequestPayment</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketRequestPayment.html">GetBucketRequestPayment</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Request
                  - Payments
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
            /{Bucket}?versioning:
              PUT:
                summary: PutBucketVersioning
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the versioning state of an
                  existing bucket.</p> <p>You can set the versioning state with
                  one of the following values:</p> <p> <b>Enabled</b>—Enables
                  versioning for the objects in the bucket. All objects added to
                  the bucket receive a unique version ID.</p> <p>
                  <b>Suspended</b>—Disables versioning for the objects in the
                  bucket. All objects added to the bucket receive the version ID
                  null.</p> <p>If the versioning state has never been set on a
                  bucket, it has no versioning state; a <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketVersioning.html">GetBucketVersioning</a>
                  request does not return a versioning state value.</p> <p>In
                  order to enable MFA Delete, you must be the bucket owner. If
                  you are the bucket owner and want to enable MFA Delete in the
                  bucket versioning configuration, you must include the
                  <code>x-amz-mfa request</code> header and the
                  <code>Status</code> and the <code>MfaDelete</code> request
                  elements in a request to set the versioning state of the
                  bucket.</p> <important> <p>If you have an object expiration
                  lifecycle configuration in your non-versioned bucket and you
                  want to maintain the same permanent delete behavior when you
                  enable versioning, you must add a noncurrent expiration
                  policy. The noncurrent expiration lifecycle configuration will
                  manage the deletes of the noncurrent object versions in the
                  version-enabled bucket. (A version-enabled bucket maintains
                  one current and zero or more noncurrent object versions.) For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html#lifecycle-and-other-bucket-config">Lifecycle
                  and Versioning</a>.</p> </important> <p>The following
                  operations are related to
                  <code>PutBucketVersioning</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketVersioning.html">GetBucketVersioning</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Versioning
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
            /{Bucket}/{Key+}?acl:
              PUT:
                summary: PutObjectAcl
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Uses the <code>acl</code> subresource
                  to set the access control list (ACL) permissions for a new or
                  existing object in an S3 bucket. You must have the
                  <code>WRITE_ACP</code> permission to set the ACL of an object.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#permissions">What
                  permissions can I grant?</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This functionality is not supported for
                  Amazon S3 on Outposts.</p> <p>Depending on your application
                  needs, you can choose to set the ACL on an object using either
                  the request body or the headers. For example, if you have an
                  existing application that updates a bucket ACL using the
                  request body, you can continue to use that approach. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html">Access
                  Control List (ACL) Overview</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <important> <p>If your bucket uses the bucket
                  owner enforced setting for S3 Object Ownership, ACLs are
                  disabled and no longer affect permissions. You must use
                  policies to grant access to your bucket and the objects in it.
                  Requests to set ACLs or update ACLs fail and return the
                  <code>AccessControlListNotSupported</code> error code.
                  Requests to read ACLs are still supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html">Controlling
                  object ownership</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </important> <dl> <dt>Permissions</dt> <dd> <p>You can set
                  access permissions using one of the following methods:</p>
                  <ul> <li> <p>Specify a canned ACL with the
                  <code>x-amz-acl</code> request header. Amazon S3 supports a
                  set of predefined ACLs, known as canned ACLs. Each canned ACL
                  has a predefined set of grantees and permissions. Specify the
                  canned ACL name as the value of <code>x-amz-ac</code>l. If you
                  use this header, you cannot use other access control-specific
                  headers in your request. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#CannedACL">Canned
                  ACL</a>.</p> </li> <li> <p>Specify access permissions
                  explicitly with the <code>x-amz-grant-read</code>,
                  <code>x-amz-grant-read-acp</code>,
                  <code>x-amz-grant-write-acp</code>, and
                  <code>x-amz-grant-full-control</code> headers. When using
                  these headers, you specify explicit access permissions and
                  grantees (Amazon Web Services accounts or Amazon S3 groups)
                  who will receive the permission. If you use these ACL-specific
                  headers, you cannot use <code>x-amz-acl</code> header to set a
                  canned ACL. These parameters map to the set of permissions
                  that Amazon S3 supports in an ACL. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html">Access
                  Control List (ACL) Overview</a>.</p> <p>You specify each
                  grantee as a type=value pair, where the type is one of the
                  following:</p> <ul> <li> <p> <code>id</code> – if the value
                  specified is the canonical user ID of an Amazon Web Services
                  account</p> </li> <li> <p> <code>uri</code> – if you are
                  granting permissions to a predefined group</p> </li> <li> <p>
                  <code>emailAddress</code> – if the value specified is the
                  email address of an Amazon Web Services account</p> <note>
                  <p>Using email addresses to specify a grantee is only
                  supported in the following Amazon Web Services Regions: </p>
                  <ul> <li> <p>US East (N. Virginia)</p> </li> <li> <p>US West
                  (N. California)</p> </li> <li> <p> US West (Oregon)</p> </li>
                  <li> <p> Asia Pacific (Singapore)</p> </li> <li> <p>Asia
                  Pacific (Sydney)</p> </li> <li> <p>Asia Pacific (Tokyo)</p>
                  </li> <li> <p>Europe (Ireland)</p> </li> <li> <p>South America
                  (São Paulo)</p> </li> </ul> <p>For a list of all the Amazon S3
                  supported Regions and endpoints, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> <p>For example, the
                  following <code>x-amz-grant-read</code> header grants list
                  objects permission to the two Amazon Web Services accounts
                  identified by their email addresses.</p> <p>
                  <code>x-amz-grant-read: emailAddress="xyz@amazon.com",
                  emailAddress="abc@amazon.com" </code> </p> </li> </ul> <p>You
                  can use either a canned ACL or specify access permissions
                  explicitly. You cannot do both.</p> </dd> <dt>Grantee
                  Values</dt> <dd> <p>You can specify the person (grantee) to
                  whom you're assigning access rights (using request elements)
                  in the following ways:</p> <ul> <li> <p>By the person's
                  ID:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="CanonicalUser"&gt;&lt;ID&gt;&lt;&gt;ID&lt;&gt;&lt;/ID&gt;&lt;DisplayName&gt;&lt;&gt;GranteesEmail&lt;&gt;&lt;/DisplayName&gt;
                  &lt;/Grantee&gt;</code> </p> <p>DisplayName is optional and
                  ignored in the request.</p> </li> <li> <p>By URI:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="Group"&gt;&lt;URI&gt;&lt;&gt;http://acs.amazonaws.com/groups/global/AuthenticatedUsers&lt;&gt;&lt;/URI&gt;&lt;/Grantee&gt;</code>
                  </p> </li> <li> <p>By Email address:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="AmazonCustomerByEmail"&gt;&lt;EmailAddress&gt;&lt;&gt;Grantees@email.com&lt;&gt;&lt;/EmailAddress&gt;lt;/Grantee&gt;</code>
                  </p> <p>The grantee is resolved to the CanonicalUser and, in a
                  response to a GET Object acl request, appears as the
                  CanonicalUser.</p> <note> <p>Using email addresses to specify
                  a grantee is only supported in the following Amazon Web
                  Services Regions: </p> <ul> <li> <p>US East (N. Virginia)</p>
                  </li> <li> <p>US West (N. California)</p> </li> <li> <p> US
                  West (Oregon)</p> </li> <li> <p> Asia Pacific (Singapore)</p>
                  </li> <li> <p>Asia Pacific (Sydney)</p> </li> <li> <p>Asia
                  Pacific (Tokyo)</p> </li> <li> <p>Europe (Ireland)</p> </li>
                  <li> <p>South America (São Paulo)</p> </li> </ul> <p>For a
                  list of all the Amazon S3 supported Regions and endpoints, see
                  <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> </dd> <dt>Versioning</dt>
                  <dd> <p>The ACL of an object is set at the object version
                  level. By default, PUT sets the ACL of the current version of
                  an object. To set the ACL of a different version, use the
                  <code>versionId</code> subresource.</p> </dd> </dl> <p>The
                  following operations are related to
                  <code>PutObjectAcl</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html">CopyObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Objects
                  - ACL
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
            /{Bucket}/{Key+}?attributes:
              GET:
                summary: GetObjectAttributes
                description: >-
                  <p>Retrieves all the metadata from an object without returning
                  the object itself. This operation is useful if you're
                  interested only in an object's metadata. </p> <p>
                  <code>GetObjectAttributes</code> combines the functionality of
                  <code>HeadObject</code> and <code>ListParts</code>. All of the
                  data returned with each of those individual calls can be
                  returned with a single call to
                  <code>GetObjectAttributes</code>.</p> <note> <p> <b>Directory
                  buckets</b> - For directory buckets, you must make requests
                  for this API operation to the Zonal endpoint. These endpoints
                  support virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket permissions</b> - To use
                  <code>GetObjectAttributes</code>, you must have READ access to
                  the object. The permissions that you need to use this
                  operation with depend on whether the bucket is versioned. If
                  the bucket is versioned, you need both the
                  <code>s3:GetObjectVersion</code> and
                  <code>s3:GetObjectVersionAttributes</code> permissions for
                  this operation. If the bucket is not versioned, you need the
                  <code>s3:GetObject</code> and
                  <code>s3:GetObjectAttributes</code> permissions. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a> in the <i>Amazon S3 User
                  Guide</i>. If the object that you request does not exist, the
                  error Amazon S3 returns depends on whether you also have the
                  <code>s3:ListBucket</code> permission.</p> <ul> <li> <p>If you
                  have the <code>s3:ListBucket</code> permission on the bucket,
                  Amazon S3 returns an HTTP status code <code>404 Not
                  Found</code> ("no such key") error.</p> </li> <li> <p>If you
                  don't have the <code>s3:ListBucket</code> permission, Amazon
                  S3 returns an HTTP status code <code>403 Forbidden</code>
                  ("access denied") error.</p> </li> </ul> </li> <li> <p>
                  <b>Directory bucket permissions</b> - To grant access to this
                  API operation on a directory bucket, we recommend that you use
                  the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Encryption</dt> <dd> <note> <p>Encryption request headers,
                  like <code>x-amz-server-side-encryption</code>, should not be
                  sent for <code>HEAD</code> requests if your object uses
                  server-side encryption with Key Management Service (KMS) keys
                  (SSE-KMS), dual-layer server-side encryption with Amazon Web
                  Services KMS keys (DSSE-KMS), or server-side encryption with
                  Amazon S3 managed encryption keys (SSE-S3). The
                  <code>x-amz-server-side-encryption</code> header is used when
                  you <code>PUT</code> an object to S3 and want to specify the
                  encryption method. If you include this header in a
                  <code>GET</code> request for an object that uses these types
                  of keys, you’ll get an HTTP <code>400 Bad Request</code>
                  error. It's because the encryption method can't be changed
                  when you retrieve the object.</p> </note> <p>If you encrypt an
                  object by using server-side encryption with customer-provided
                  encryption keys (SSE-C) when you store the object in Amazon
                  S3, then when you retrieve the metadata from the object, you
                  must use the following headers to provide the encryption key
                  for the server to be able to retrieve the object's metadata.
                  The headers are: </p> <ul> <li> <p>
                  <code>x-amz-server-side-encryption-customer-algorithm</code>
                  </p> </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key</code> </p>
                  </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key-MD5</code>
                  </p> </li> </ul> <p>For more information about SSE-C, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerSideEncryptionCustomerKeys.html">Server-Side
                  Encryption (Using Customer-Provided Encryption Keys)</a> in
                  the <i>Amazon S3 User Guide</i>.</p> <note> <p> <b>Directory
                  bucket permissions</b> - For directory buckets, only
                  server-side encryption with Amazon S3 managed keys (SSE-S3)
                  (<code>AES256</code>) is supported.</p> </note> </dd>
                  <dt>Versioning</dt> <dd> <p> <b>Directory buckets</b> - S3
                  Versioning isn't enabled and supported for directory buckets.
                  For this API operation, only the <code>null</code> value of
                  the version ID is supported by directory buckets. You can only
                  specify <code>null</code> to the <code>versionId</code> query
                  parameter in the request.</p> </dd> <dt>Conditional request
                  headers</dt> <dd> <p>Consider the following when using request
                  headers:</p> <ul> <li> <p>If both of the <code>If-Match</code>
                  and <code>If-Unmodified-Since</code> headers are present in
                  the request as follows, then Amazon S3 returns the HTTP status
                  code <code>200 OK</code> and the data requested:</p> <ul> <li>
                  <p> <code>If-Match</code> condition evaluates to
                  <code>true</code>.</p> </li> <li> <p>
                  <code>If-Unmodified-Since</code> condition evaluates to
                  <code>false</code>.</p> </li> </ul> <p>For more information
                  about conditional requests, see <a
                  href="https://tools.ietf.org/html/rfc7232">RFC 7232</a>.</p>
                  </li> <li> <p>If both of the <code>If-None-Match</code> and
                  <code>If-Modified-Since</code> headers are present in the
                  request as follows, then Amazon S3 returns the HTTP status
                  code <code>304 Not Modified</code>:</p> <ul> <li> <p>
                  <code>If-None-Match</code> condition evaluates to
                  <code>false</code>.</p> </li> <li> <p>
                  <code>If-Modified-Since</code> condition evaluates to
                  <code>true</code>.</p> </li> </ul> <p>For more information
                  about conditional requests, see <a
                  href="https://tools.ietf.org/html/rfc7232">RFC 7232</a>.</p>
                  </li> </ul> </dd> <dt>HTTP Host header syntax</dt> <dd> <p>
                  <b>Directory buckets </b> - The HTTP Host header syntax is
                  <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following actions are related to
                  <code>GetObjectAttributes</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectAcl.html">GetObjectAcl</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectLegalHold.html">GetObjectLegalHold</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectLockConfiguration.html">GetObjectLockConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectRetention.html">GetObjectRetention</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html">GetObjectTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadObject.html">HeadObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Objects
                  - Attributes
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
            /{Bucket}/{Key+}?legal-hold:
              PUT:
                summary: PutObjectLegalHold
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Applies a legal hold configuration to
                  the specified object. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Locking
                  Objects</a>.</p> <p>This functionality is not supported for
                  Amazon S3 on Outposts.</p>
                tags:
                  - Put
                  - Objects
                  - Legal
                  - Hold
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
            /{Bucket}?object-lock:
              PUT:
                summary: PutObjectLockConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Places an Object Lock configuration on
                  the specified bucket. The rule specified in the Object Lock
                  configuration will be applied by default to every new object
                  placed in the specified bucket. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Locking
                  Objects</a>. </p> <note> <ul> <li> <p>The
                  <code>DefaultRetention</code> settings require both a mode and
                  a period.</p> </li> <li> <p>The <code>DefaultRetention</code>
                  period can be either <code>Days</code> or <code>Years</code>
                  but you must select one. You cannot specify <code>Days</code>
                  and <code>Years</code> at the same time.</p> </li> <li> <p>You
                  can enable Object Lock for new or existing buckets. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock-configure.html">Configuring
                  Object Lock</a>.</p> </li> </ul> </note>
                tags:
                  - Put
                  - Objects
                  - Locks
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
            /{Bucket}/{Key+}?retention:
              PUT:
                summary: PutObjectRetention
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Places an Object Retention
                  configuration on an object. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Locking
                  Objects</a>. Users or accounts require the
                  <code>s3:PutObjectRetention</code> permission in order to
                  place an Object Retention configuration on objects. Bypassing
                  a Governance Retention configuration requires the
                  <code>s3:BypassGovernanceRetention</code> permission. </p>
                  <p>This functionality is not supported for Amazon S3 on
                  Outposts.</p>
                tags:
                  - Put
                  - Objects
                  - Retention
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
            /{Bucket}/{Key+}?torrent:
              GET:
                summary: GetObjectTorrent
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns torrent files from a bucket.
                  BitTorrent can save you bandwidth when you're distributing
                  large files.</p> <note> <p>You can get torrent only for
                  objects that are less than 5 GB in size, and that are not
                  encrypted using server-side encryption with a
                  customer-provided encryption key.</p> </note> <p>To use GET,
                  you must have READ access to the object.</p> <p>This
                  functionality is not supported for Amazon S3 on Outposts.</p>
                  <p>The following action is related to
                  <code>GetObjectTorrent</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Objects
                  - Torrent
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
            /:
              GET:
                summary: ListDirectoryBuckets
                description: >-
                  <p>Returns a list of all Amazon S3 directory buckets owned by
                  the authenticated sender of the request. For more information
                  about directory buckets, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/directory-buckets-overview.html">Directory
                  buckets</a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>
                  <b>Directory buckets </b> - For directory buckets, you must
                  make requests for this API operation to the Regional endpoint.
                  These endpoints support path-style requests in the format
                  <code>https://s3express-control.<i>region_code</i>.amazonaws.com/<i>bucket-name</i>
                  </code>. Virtual-hosted-style requests aren't supported. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3express:ListAllMyDirectoryBuckets</code>
                  permission in an IAM identity-based policy instead of a bucket
                  policy. Cross-account access to this API operation isn't
                  supported. This operation can only be performed by the Amazon
                  Web Services account that owns the resource. For more
                  information about directory bucket policies and permissions,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam.html">Amazon
                  Web Services Identity and Access Management (IAM) for S3
                  Express One Zone</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </dd> <dt>HTTP Host header syntax</dt> <dd> <p> <b>Directory
                  buckets </b> - The HTTP Host header syntax is
                  <code>s3express-control.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl>
                tags:
                  - Lists
                  - Directory
                  - Buckets
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
            /{Bucket}?uploads:
              GET:
                summary: ListMultipartUploads
                description: >-
                  <p>This operation lists in-progress multipart uploads in a
                  bucket. An in-progress multipart upload is a multipart upload
                  that has been initiated by the
                  <code>CreateMultipartUpload</code> request, but has not yet
                  been completed or aborted.</p> <note> <p> <b>Directory
                  buckets</b> - If multipart uploads in a directory bucket are
                  in progress, you can't delete the bucket until all the
                  in-progress multipart uploads are aborted or completed. </p>
                  </note> <p>The <code>ListMultipartUploads</code> operation
                  returns a maximum of 1,000 multipart uploads in the response.
                  The limit of 1,000 multipart uploads is also the default
                  value. You can further limit the number of uploads in a
                  response by specifying the <code>max-uploads</code> request
                  parameter. If there are more than 1,000 multipart uploads that
                  satisfy your <code>ListMultipartUploads</code> request, the
                  response returns an <code>IsTruncated</code> element with the
                  value of <code>true</code>, a <code>NextKeyMarker</code>
                  element, and a <code>NextUploadIdMarker</code> element. To
                  list the remaining multipart uploads, you need to make
                  subsequent <code>ListMultipartUploads</code> requests. In
                  these requests, include two query parameters:
                  <code>key-marker</code> and <code>upload-id-marker</code>. Set
                  the value of <code>key-marker</code> to the
                  <code>NextKeyMarker</code> value from the previous response.
                  Similarly, set the value of <code>upload-id-marker</code> to
                  the <code>NextUploadIdMarker</code> value from the previous
                  response.</p> <note> <p> <b>Directory buckets</b> - The
                  <code>upload-id-marker</code> element and the
                  <code>NextUploadIdMarker</code> element aren't supported by
                  directory buckets. To list the additional multipart uploads,
                  you only need to set the value of <code>key-marker</code> to
                  the <code>NextKeyMarker</code> value from the previous
                  response. </p> </note> <p>For more information about multipart
                  uploads, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html">Uploading
                  Objects Using Multipart Upload</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <p> <b>Directory buckets</b> - For
                  directory buckets, you must make requests for this API
                  operation to the Zonal endpoint. These endpoints support
                  virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket permissions</b> - For
                  information about permissions required to use the multipart
                  upload API, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuAndPermissions.html">Multipart
                  Upload and Permissions</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b>Directory bucket
                  permissions</b> - To grant access to this API operation on a
                  directory bucket, we recommend that you use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Sorting of multipart uploads in response</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket</b> - In the
                  <code>ListMultipartUploads</code> response, the multipart
                  uploads are sorted based on two criteria:</p> <ul> <li>
                  <p>Key-based sorting - Multipart uploads are initially sorted
                  in ascending order based on their object keys.</p> </li> <li>
                  <p>Time-based sorting - For uploads that share the same object
                  key, they are further sorted in ascending order based on the
                  upload initiation time. Among uploads with the same key, the
                  one that was initiated first will appear before the ones that
                  were initiated later.</p> </li> </ul> </li> <li> <p>
                  <b>Directory bucket</b> - In the
                  <code>ListMultipartUploads</code> response, the multipart
                  uploads aren't sorted lexicographically based on the object
                  keys. </p> </li> </ul> </dd> <dt>HTTP Host header syntax</dt>
                  <dd> <p> <b>Directory buckets </b> - The HTTP Host header
                  syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>ListMultipartUploads</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateMultipartUpload.html">CreateMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Multipart
                  - Uploads
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
            /{Bucket}?versions:
              GET:
                summary: ListObjectVersions
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns metadata about all versions of
                  the objects in a bucket. You can also use request parameters
                  as selection criteria to return metadata about a subset of all
                  the object versions.</p> <important> <p> To use this
                  operation, you must have permission to perform the
                  <code>s3:ListBucketVersions</code> action. Be aware of the
                  name difference. </p> </important> <note> <p> A <code>200
                  OK</code> response can contain valid or invalid XML. Make sure
                  to design your application to parse the contents of the
                  response and handle it appropriately.</p> </note> <p>To use
                  this operation, you must have READ access to the bucket.</p>
                  <p>The following operations are related to
                  <code>ListObjectVersions</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html">ListObjectsV2</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObject.html">DeleteObject</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Objects
                  - Versions
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
            /{Bucket}?list-type=2:
              GET:
                summary: ListObjectsV2
                description: >-
                  <p>Returns some or all (up to 1,000) of the objects in a
                  bucket with each request. You can use the request parameters
                  as selection criteria to return a subset of the objects in a
                  bucket. A <code>200 OK</code> response can contain valid or
                  invalid XML. Make sure to design your application to parse the
                  contents of the response and handle it appropriately. For more
                  information about listing objects, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ListingKeysUsingAPIs.html">Listing
                  object keys programmatically</a> in the <i>Amazon S3 User
                  Guide</i>. To get a list of your buckets, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html">ListBuckets</a>.</p>
                  <note> <p> <b>Directory buckets</b> - For directory buckets,
                  you must make requests for this API operation to the Zonal
                  endpoint. These endpoints support virtual-hosted-style
                  requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket permissions</b> - To use
                  this operation, you must have READ access to the bucket. You
                  must have permission to perform the <code>s3:ListBucket</code>
                  action. The bucket owner has this permission by default and
                  can grant this permission to others. For more information
                  about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> <li> <p> <b>Directory
                  bucket permissions</b> - To grant access to this API operation
                  on a directory bucket, we recommend that you use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Sorting order of returned objects</dt> <dd> <ul> <li> <p>
                  <b>General purpose bucket</b> - For general purpose buckets,
                  <code>ListObjectsV2</code> returns objects in lexicographical
                  order based on their key names.</p> </li> <li> <p>
                  <b>Directory bucket</b> - For directory buckets,
                  <code>ListObjectsV2</code> does not return objects in
                  lexicographical order.</p> </li> </ul> </dd> <dt>HTTP Host
                  header syntax</dt> <dd> <p> <b>Directory buckets </b> - The
                  HTTP Host header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <important> <p>This section describes the latest
                  revision of this action. We recommend that you use this
                  revised API operation for application development. For
                  backward compatibility, Amazon S3 continues to support the
                  prior version of this API operation, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjects.html">ListObjects</a>.</p>
                  </important> <p>The following operations are related to
                  <code>ListObjectsV2</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Objects
                  - V2
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
            /{Bucket}/{Key+}?restore:
              POST:
                summary: RestoreObject
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Restores an archived copy of an object
                  back into Amazon S3</p> <p>This functionality is not supported
                  for Amazon S3 on Outposts.</p> <p>This action performs the
                  following types of requests: </p> <ul> <li> <p>
                  <code>select</code> - Perform a select query on an archived
                  object</p> </li> <li> <p> <code>restore an archive</code> -
                  Restore an archived object</p> </li> </ul> <p>For more
                  information about the <code>S3</code> structure in the request
                  body, see the following:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/S3_ACLs_UsingACLs.html">Managing
                  Access with ACLs</a> in the <i>Amazon S3 User Guide</i> </p>
                  </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html">Protecting
                  Data Using Server-Side Encryption</a> in the <i>Amazon S3 User
                  Guide</i> </p> </li> </ul> <p>Define the SQL expression for
                  the <code>SELECT</code> type of restoration for your query in
                  the request body's <code>SelectParameters</code> structure.
                  You can use expressions like the following examples.</p> <ul>
                  <li> <p>The following expression returns all records from the
                  specified object.</p> <p> <code>SELECT * FROM Object</code>
                  </p> </li> <li> <p>Assuming that you are not using any headers
                  for data stored in the object, you can specify columns with
                  positional headers.</p> <p> <code>SELECT s._1, s._2 FROM
                  Object s WHERE s._3 &gt; 100</code> </p> </li> <li> <p>If you
                  have headers and you set the <code>fileHeaderInfo</code> in
                  the <code>CSV</code> structure in the request body to
                  <code>USE</code>, you can specify headers in the query. (If
                  you set the <code>fileHeaderInfo</code> field to
                  <code>IGNORE</code>, the first row is skipped for the query.)
                  You cannot mix ordinal positions with header column names.
                  </p> <p> <code>SELECT s.Id, s.FirstName, s.SSN FROM S3Object
                  s</code> </p> </li> </ul> <p>When making a select request, you
                  can also do the following:</p> <ul> <li> <p>To expedite your
                  queries, specify the <code>Expedited</code> tier. For more
                  information about tiers, see "Restoring Archives," later in
                  this topic.</p> </li> <li> <p>Specify details about the data
                  serialization format of both the input object that is being
                  queried and the serialization of the CSV-encoded query
                  results.</p> </li> </ul> <p>The following are additional
                  important facts about the select feature:</p> <ul> <li> <p>The
                  output results are new Amazon S3 objects. Unlike archive
                  retrievals, they are stored until explicitly deleted-manually
                  or through a lifecycle configuration.</p> </li> <li> <p>You
                  can issue more than one select request on the same Amazon S3
                  object. Amazon S3 doesn't duplicate requests, so avoid issuing
                  duplicate requests.</p> </li> <li> <p> Amazon S3 accepts a
                  select request even if the object has already been restored. A
                  select request doesn’t return error response
                  <code>409</code>.</p> </li> </ul> <dl> <dt>Permissions</dt>
                  <dd> <p>To use this operation, you must have permissions to
                  perform the <code>s3:RestoreObject</code> action. The bucket
                  owner has this permission by default and can grant this
                  permission to others. For more information about permissions,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </dd> <dt>Restoring
                  objects</dt> <dd> <p>Objects that you archive to the S3
                  Glacier Flexible Retrieval Flexible Retrieval or S3 Glacier
                  Deep Archive storage class, and S3 Intelligent-Tiering Archive
                  or S3 Intelligent-Tiering Deep Archive tiers, are not
                  accessible in real time. For objects in the S3 Glacier
                  Flexible Retrieval Flexible Retrieval or S3 Glacier Deep
                  Archive storage classes, you must first initiate a restore
                  request, and then wait until a temporary copy of the object is
                  available. If you want a permanent copy of the object, create
                  a copy of it in the Amazon S3 Standard storage class in your
                  S3 bucket. To access an archived object, you must restore the
                  object for the duration (number of days) that you specify. For
                  objects in the Archive Access or Deep Archive Access tiers of
                  S3 Intelligent-Tiering, you must first initiate a restore
                  request, and then wait until the object is moved into the
                  Frequent Access tier.</p> <p>To restore a specific object
                  version, you can provide a version ID. If you don't provide a
                  version ID, Amazon S3 restores the current version.</p>
                  <p>When restoring an archived object, you can specify one of
                  the following data access tier options in the
                  <code>Tier</code> element of the request body: </p> <ul> <li>
                  <p> <code>Expedited</code> - Expedited retrievals allow you to
                  quickly access your data stored in the S3 Glacier Flexible
                  Retrieval Flexible Retrieval storage class or S3
                  Intelligent-Tiering Archive tier when occasional urgent
                  requests for restoring archives are required. For all but the
                  largest archived objects (250 MB+), data accessed using
                  Expedited retrievals is typically made available within 1–5
                  minutes. Provisioned capacity ensures that retrieval capacity
                  for Expedited retrievals is available when you need it.
                  Expedited retrievals and provisioned capacity are not
                  available for objects stored in the S3 Glacier Deep Archive
                  storage class or S3 Intelligent-Tiering Deep Archive tier.</p>
                  </li> <li> <p> <code>Standard</code> - Standard retrievals
                  allow you to access any of your archived objects within
                  several hours. This is the default option for retrieval
                  requests that do not specify the retrieval option. Standard
                  retrievals typically finish within 3–5 hours for objects
                  stored in the S3 Glacier Flexible Retrieval Flexible Retrieval
                  storage class or S3 Intelligent-Tiering Archive tier. They
                  typically finish within 12 hours for objects stored in the S3
                  Glacier Deep Archive storage class or S3 Intelligent-Tiering
                  Deep Archive tier. Standard retrievals are free for objects
                  stored in S3 Intelligent-Tiering.</p> </li> <li> <p>
                  <code>Bulk</code> - Bulk retrievals free for objects stored in
                  the S3 Glacier Flexible Retrieval and S3 Intelligent-Tiering
                  storage classes, enabling you to retrieve large amounts, even
                  petabytes, of data at no cost. Bulk retrievals typically
                  finish within 5–12 hours for objects stored in the S3 Glacier
                  Flexible Retrieval Flexible Retrieval storage class or S3
                  Intelligent-Tiering Archive tier. Bulk retrievals are also the
                  lowest-cost retrieval option when restoring objects from S3
                  Glacier Deep Archive. They typically finish within 48 hours
                  for objects stored in the S3 Glacier Deep Archive storage
                  class or S3 Intelligent-Tiering Deep Archive tier. </p> </li>
                  </ul> <p>For more information about archive retrieval options
                  and provisioned capacity for <code>Expedited</code> data
                  access, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/restoring-objects.html">Restoring
                  Archived Objects</a> in the <i>Amazon S3 User Guide</i>. </p>
                  <p>You can use Amazon S3 restore speed upgrade to change the
                  restore speed to a faster speed while it is in progress. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/restoring-objects.html#restoring-objects-upgrade-tier.title.html">
                  Upgrading the speed of an in-progress restore</a> in the
                  <i>Amazon S3 User Guide</i>. </p> <p>To get the status of
                  object restoration, you can send a <code>HEAD</code> request.
                  Operations return the <code>x-amz-restore</code> header, which
                  provides information about the restoration status, in the
                  response. You can use Amazon S3 event notifications to notify
                  you when a restore is initiated or completed. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html">Configuring
                  Amazon S3 Event Notifications</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>After restoring an archived object, you can
                  update the restoration period by reissuing the request with a
                  new period. Amazon S3 updates the restoration period relative
                  to the current time and charges only for the request-there are
                  no data transfer charges. You cannot update the restoration
                  period when Amazon S3 is actively processing your current
                  restore request for the object.</p> <p>If your bucket has a
                  lifecycle configuration with a rule that includes an
                  expiration action, the object expiration overrides the life
                  span that you specify in a restore request. For example, if
                  you restore an object copy for 10 days, but the object is
                  scheduled to expire in 3 days, Amazon S3 deletes the object in
                  3 days. For more information about lifecycle configuration,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html">Object
                  Lifecycle Management</a> in <i>Amazon S3 User Guide</i>.</p>
                  </dd> <dt>Responses</dt> <dd> <p>A successful action returns
                  either the <code>200 OK</code> or <code>202 Accepted</code>
                  status code. </p> <ul> <li> <p>If the object is not previously
                  restored, then Amazon S3 returns <code>202 Accepted</code> in
                  the response. </p> </li> <li> <p>If the object is previously
                  restored, Amazon S3 returns <code>200 OK</code> in the
                  response. </p> </li> </ul> <ul> <li> <p>Special errors:</p>
                  <ul> <li> <p> <i>Code: RestoreAlreadyInProgress</i> </p> </li>
                  <li> <p> <i>Cause: Object restore is already in progress.
                  (This error does not apply to SELECT type requests.)</i> </p>
                  </li> <li> <p> <i>HTTP Status Code: 409 Conflict</i> </p>
                  </li> <li> <p> <i>SOAP Fault Code Prefix: Client</i> </p>
                  </li> </ul> </li> <li> <ul> <li> <p> <i>Code:
                  GlacierExpeditedRetrievalNotAvailable</i> </p> </li> <li> <p>
                  <i>Cause: expedited retrievals are currently not available.
                  Try again later. (Returned if there is insufficient capacity
                  to process the Expedited request. This error applies only to
                  Expedited retrievals and not to S3 Standard or Bulk
                  retrievals.)</i> </p> </li> <li> <p> <i>HTTP Status Code:
                  503</i> </p> </li> <li> <p> <i>SOAP Fault Code Prefix: N/A</i>
                  </p> </li> </ul> </li> </ul> </dd> </dl> <p>The following
                  operations are related to <code>RestoreObject</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketNotificationConfiguration.html">GetBucketNotificationConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Restore
                  - Objects
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
                  - '?restore'
            /{Bucket}/{Key+}?select&select-type=2:
              POST:
                summary: SelectObjectContent
                description: "<note> <p>This operation is not supported by directory buckets.</p> </note> <p>This action filters the contents of an Amazon S3 object based on a simple structured query language (SQL) statement. In the request, along with the SQL expression, you must also specify a data serialization format (JSON, CSV, or Apache Parquet) of the object. Amazon S3 uses this format to parse object data into records, and returns only records that match the specified SQL expression. You must also specify the data serialization format for the response.</p> <p>This functionality is not supported for Amazon S3 on Outposts.</p> <p>For more information about Amazon S3 Select, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/selecting-content-from-objects.html\">Selecting Content from Objects</a> and <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-glacier-select-sql-reference-select.html\">SELECT Command</a> in the <i>Amazon S3 User Guide</i>.</p> <p/> <dl> <dt>Permissions</dt> <dd> <p>You must have the <code>s3:GetObject</code> permission for this operation.\_Amazon S3 Select does not support anonymous access. For more information about permissions, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html\">Specifying Permissions in a Policy</a> in the <i>Amazon S3 User Guide</i>.</p> </dd> <dt>Object Data Formats</dt> <dd> <p>You can use Amazon S3 Select to query objects that have the following format properties:</p> <ul> <li> <p> <i>CSV, JSON, and Parquet</i> - Objects must be in CSV, JSON, or Parquet format.</p> </li> <li> <p> <i>UTF-8</i> - UTF-8 is the only encoding type Amazon S3 Select supports.</p> </li> <li> <p> <i>GZIP or BZIP2</i> - CSV and JSON files can be compressed using GZIP or BZIP2. GZIP and BZIP2 are the only compression formats that Amazon S3 Select supports for CSV and JSON files. Amazon S3 Select supports columnar compression for Parquet using GZIP or Snappy. Amazon S3 Select does not support whole-object compression for Parquet objects.</p> </li> <li> <p> <i>Server-side encryption</i> - Amazon S3 Select supports querying objects that are protected with server-side encryption.</p> <p>For objects that are encrypted with customer-provided encryption keys (SSE-C), you must use HTTPS, and you must use the headers that are documented in the <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html\">GetObject</a>. For more information about SSE-C, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerSideEncryptionCustomerKeys.html\">Server-Side Encryption (Using Customer-Provided Encryption Keys)</a> in the <i>Amazon S3 User Guide</i>.</p> <p>For objects that are encrypted with Amazon S3 managed keys (SSE-S3) and Amazon Web Services KMS keys (SSE-KMS), server-side encryption is handled transparently, so you don't need to specify anything. For more information about server-side encryption, including SSE-S3 and SSE-KMS, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html\">Protecting Data Using Server-Side Encryption</a> in the <i>Amazon S3 User Guide</i>.</p> </li> </ul> </dd> <dt>Working with the Response Body</dt> <dd> <p>Given the response size is unknown, Amazon S3 Select streams the response as a series of messages and includes a <code>Transfer-Encoding</code> header with <code>chunked</code> as its value in the response. For more information, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/RESTSelectObjectAppendix.html\">Appendix: SelectObjectContent Response</a>.</p> </dd> <dt>GetObject Support</dt> <dd> <p>The <code>SelectObjectContent</code> action does not support the following <code>GetObject</code> functionality. For more information, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html\">GetObject</a>.</p> <ul> <li> <p> <code>Range</code>: Although you can specify a scan range for an Amazon S3 Select request (see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_SelectObjectContent.html#AmazonS3-SelectObjectContent-request-ScanRange\">SelectObjectContentRequest - ScanRange</a> in the request parameters), you cannot specify the range of bytes of an object to return. </p> </li> <li> <p>The <code>GLACIER</code>, <code>DEEP_ARCHIVE</code>, and <code>REDUCED_REDUNDANCY</code> storage classes, or the <code>ARCHIVE_ACCESS</code> and <code>DEEP_ARCHIVE_ACCESS</code> access tiers of the <code>INTELLIGENT_TIERING</code> storage class: You cannot query objects in the <code>GLACIER</code>, <code>DEEP_ARCHIVE</code>, or <code>REDUCED_REDUNDANCY</code> storage classes, nor objects in the <code>ARCHIVE_ACCESS</code> or <code>DEEP_ARCHIVE_ACCESS</code> access tiers of the <code>INTELLIGENT_TIERING</code> storage class. For more information about storage classes, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html\">Using Amazon S3 storage classes</a> in the <i>Amazon S3 User Guide</i>.</p> </li> </ul> </dd> <dt>Special Errors</dt> <dd> <p>For a list of special errors for this operation, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#SelectObjectContentErrorCodeList\">List of SELECT Object Content Error Codes</a> </p> </dd> </dl> <p>The following operations are related to <code>SelectObjectContent</code>:</p> <ul> <li> <p> <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html\">GetObject</a> </p> </li> <li> <p> <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLifecycleConfiguration.html\">GetBucketLifecycleConfiguration</a> </p> </li> <li> <p> <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html\">PutBucketLifecycleConfiguration</a> </p> </li> </ul>"
                tags:
                  - Select
                  - Objects
                  - Content
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
                  - '?restore'
                  - '?select&select'
            /WriteGetObjectResponse:
              POST:
                summary: WriteGetObjectResponse
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Passes transformed objects to a
                  <code>GetObject</code> operation when using Object Lambda
                  access points. For information about Object Lambda access
                  points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/transforming-objects.html">Transforming
                  objects with Object Lambda access points</a> in the <i>Amazon
                  S3 User Guide</i>.</p> <p>This operation supports metadata
                  that can be returned by <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>,
                  in addition to <code>RequestRoute</code>,
                  <code>RequestToken</code>, <code>StatusCode</code>,
                  <code>ErrorCode</code>, and <code>ErrorMessage</code>. The
                  <code>GetObject</code> response metadata is supported so that
                  the <code>WriteGetObjectResponse</code> caller, typically an
                  Lambda function, can provide the same metadata when it
                  internally invokes <code>GetObject</code>. When
                  <code>WriteGetObjectResponse</code> is called by a
                  customer-owned Lambda function, the metadata returned to the
                  end user <code>GetObject</code> call might differ from what
                  Amazon S3 would normally return.</p> <p>You can include any
                  number of metadata headers. When including a metadata header,
                  it should be prefaced with <code>x-amz-meta</code>. For
                  example, <code>x-amz-meta-my-custom-header:
                  MyCustomValue</code>. The primary use case for this is to
                  forward <code>GetObject</code> metadata.</p> <p>Amazon Web
                  Services provides some prebuilt Lambda functions that you can
                  use with S3 Object Lambda to detect and redact personally
                  identifiable information (PII) and decompress S3 objects.
                  These Lambda functions are available in the Amazon Web
                  Services Serverless Application Repository, and can be
                  selected through the Amazon Web Services Management Console
                  when you create your Object Lambda access point.</p>
                  <p>Example 1: PII Access Control - This Lambda function uses
                  Amazon Comprehend, a natural language processing (NLP) service
                  using machine learning to find insights and relationships in
                  text. It automatically detects personally identifiable
                  information (PII) such as names, addresses, dates, credit card
                  numbers, and social security numbers from documents in your
                  Amazon S3 bucket. </p> <p>Example 2: PII Redaction - This
                  Lambda function uses Amazon Comprehend, a natural language
                  processing (NLP) service using machine learning to find
                  insights and relationships in text. It automatically redacts
                  personally identifiable information (PII) such as names,
                  addresses, dates, credit card numbers, and social security
                  numbers from documents in your Amazon S3 bucket. </p>
                  <p>Example 3: Decompression - The Lambda function
                  S3ObjectLambdaDecompression, is equipped to decompress objects
                  stored in S3 in one of six compressed file formats including
                  bzip2, gzip, snappy, zlib, zstandard and ZIP. </p> <p>For
                  information on how to view and use these functions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/olap-examples.html">Using
                  Amazon Web Services built Lambda functions</a> in the
                  <i>Amazon S3 User Guid
                tags:
                  - Write
                  - Get
                  - Objects
                  - Responses
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
                  - '?restore'
                  - '?select&select'
                  - Write
                  - Get
                  - Objects
                  - Respon
    overlays:
      - type: APIs.io Search
        url: overlays/s3-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3
  - name: securityhub
    description: >-
      <p>Security Hub provides you with a comprehensive view of your security
      state in Amazon Web Services and helps you assess your Amazon Web Services
      environment against security industry standards and best practices.</p>
      <p>Security Hub collects security data across Amazon Web Services
      accounts, Amazon Web Services, and supported third-party products and
      helps you analyze your security trends and identify the highest priority
      security issues.</p> <p>To help you manage the security state of your
      organization, Security Hub supports multiple security standards. These
      include the Amazon Web Services Foundational Security Best Practices
      (FSBP) standard developed by Amazon Web Services, and external compliance
      frameworks such as the Center for Internet Security (CIS), the Payment
      Card Industry Data Security Standard (PCI DSS), and the National Institute
      of Standards and Technology (NIST). Each standard includes several
      security controls, each of which represents a security best practice.
      Security Hub runs checks against security controls and generates control
      findings to help you assess your compliance against security best
      practices.</p> <p>In addition to generating control findings, Security Hub
      also receives findings from other Amazon Web Services, such as Amazon
      GuardDuty and Amazon Inspector, and supported third-party products. This
      gives you a single pane of glass into a variety of security-related
      issues. You can also send Security Hub findings to other Amazon Web
      Services and supported third-party products.</p> <p>Security Hub offers
      automation features that help you triage and remediate security issues.
      For example, you can use automation rules to automatically update critical
      findings when a security check fails. You can also leverage the
      integration with Amazon EventBridge to trigger automatic responses to
      specific findings.</p> <p>This guide, the <i>Security Hub API
      Reference</i>, provides information about the Security Hub API. This
      includes supported resources, HTTP methods, parameters, and schemas. If
      you're new to Security Hub, you might find it helpful to also review the
      <a
      href="https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html">
      <i>Security Hub User Guide</i> </a>. The user guide explains key concepts
      and provides procedures that demonstrate how to use Security Hub features.
      It also provides information about topics such as integrating Security Hub
      with other Amazon Web Services.</p> <p>In addition to interacting with
      Security Hub by making calls to the Security Hub API, you can use a
      current version of an Amazon Web Services command line tool or SDK. Amazon
      Web Services provides tools and SDKs that consist of libraries and sample
      code for various languages and platforms, such as PowerShell, Java, Go,
      Python, C++, and .NET. These tools and SDKs provide convenient,
      programmatic access to Security Hub and other Amazon Web Services . They
      also handle tasks such as signing requests, managing errors, and retrying
      requests automatically. For information about installing and using the
      Amazon Web Services tools and SDKs, see <a
      href="http://aws.amazon.com/developer/tools/">Tools to Build on Amazon Web
      Services</a>.</p> <p>With the exception of operations that are related to
      central configuration, Security Hub API requests are executed only in the
      Amazon Web Services Region that is currently active or in the specific
      Amazon Web Services Region that you specify in your request. Any
      configuration or settings change that results from the operation is
      applied only to that Region. To make the same change in other Regions,
      call the same API operation in each Region in which you want to apply the
      change. When you use central configuration, API requests for enabling
      Security Hub, standards, and controls are executed in the home Region and
      all linked Regions. For a list of central configuration operations, see
      the <a
      href="https://docs.aws.amazon.com/securityhub/latest/userguide/central-configuration-intro.html#central-configuration-concepts">Central
      configuration terms and concepts</a> section of the <i>Security Hub User
      Guide</i>.</p> <p>The following throttling limits apply to Security Hub
      API operations.</p> <ul> <li> <p> <code>BatchEnableStandards</code> -
      <code>RateLimit</code> of 1 request per second. <code>BurstLimit</code> of
      1 request per second.</p> </li> <li> <p> <code>GetFindings</code> -
      <code>RateLimit</code> of 3 requests per second. <code>BurstLimit</code>
      of 6 requests per second.</p> </li> <li> <p>
      <code>BatchImportFindings</code> - <code>RateLimit</code> of 10 requests
      per second. <code>BurstLimit</code> of 30 requests per second.</p> </li>
      <li> <p> <code>BatchUpdateFindings</code> - <code>RateLimit</code> of 10
      requests per second. <code>BurstLimit</code> of 30 requests per
      second.</p> </li> <li> <p> <code>UpdateStandardsControl</code> -
      <code>RateLimit</code> of 1 request per second. <code>BurstLimit</code> of
      5 requests per second.</p> </li> <li> <p>All other operations -
      <code>RateLimit</code> of 10 requests per second. <code>BurstLimit</code>
      of 30 requests per second.</p> </li> </ul>
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
            title: securityhub
          paths:
            /administrator:
              GET:
                summary: GetAdministratorAccount
                description: >-
                  <p>Provides the details for the Security Hub administrator
                  account for the current member account.</p> <p>Can be used by
                  both member accounts that are managed using Organizations and
                  accounts that were invited manually.</p>
                tags:
                  - Get
                  - Administrator
                  - Account
                  - Administrator
            /master:
              GET:
                summary: GetMasterAccount
                description: >-
                  <p>This method is deprecated. Instead, use
                  <code>GetAdministratorAccount</code>.</p> <p>The Security Hub
                  console continues to use <code>GetMasterAccount</code>. It
                  will eventually change to use
                  <code>GetAdministratorAccount</code>. Any IAM policies that
                  specifically control access to this function must continue to
                  use <code>GetMasterAccount</code>. You should also add
                  <code>GetAdministratorAccount</code> to your policies to
                  ensure that the correct permissions are in place after the
                  console begins to use
                  <code>GetAdministratorAccount</code>.</p> <p>Provides the
                  details for the Security Hub administrator account for the
                  current member account.</p> <p>Can be used by both member
                  accounts that are managed using Organizations and accounts
                  that were invited manually.</p>
                tags:
                  - Get
                  - Master
                  - Account
                  - Administrator
                  - Master
            /automationrules/delete:
              POST:
                summary: BatchDeleteAutomationRules
                description: <p> Deletes one or more automation rules. </p>
                tags:
                  - Batches
                  - Delete
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
            /standards/deregister:
              POST:
                summary: BatchDisableStandards
                description: >-
                  <p>Disables the standards specified by the provided
                  <code>StandardsSubscriptionArns</code>.</p> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-standards.html">Security
                  Standards</a> section of the <i>Security Hub User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Disable
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
            /standards/register:
              POST:
                summary: BatchEnableStandards
                description: >-
                  <p>Enables the standards specified by the provided
                  <code>StandardsArn</code>. To obtain the ARN for a standard,
                  use the <code>DescribeStandards</code> operation.</p> <p>For
                  more information, see the <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-standards.html">Security
                  Standards</a> section of the <i>Security Hub User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Enable
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
            /automationrules/get:
              POST:
                summary: BatchGetAutomationRules
                description: >-
                  <p> Retrieves a list of details for automation rules based on
                  rule Amazon Resource Names (ARNs). </p>
                tags:
                  - Batches
                  - Get
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
            /configurationPolicyAssociation/batchget:
              POST:
                summary: BatchGetConfigurationPolicyAssociations
                description: >-
                  <p> Returns associations between an Security Hub configuration
                  and a batch of target accounts, organizational units, or the
                  root. Only the Security Hub delegated administrator can invoke
                  this operation from the home Region. A configuration can refer
                  to a configuration policy or to a self-managed configuration.
                  </p>
                tags:
                  - Batches
                  - Get
                  - Configurations
                  - Policies
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
            /securityControls/batchGet:
              POST:
                summary: BatchGetSecurityControls
                description: >-
                  <p> Provides details about a batch of security controls for
                  the current Amazon Web Services account and Amazon Web
                  Services Region. </p>
                tags:
                  - Batches
                  - Get
                  - Security
                  - Controls
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
            /associations/batchGet:
              POST:
                summary: BatchGetStandardsControlAssociations
                description: >-
                  <p> For a batch of security controls and standards, identifies
                  whether each control is currently enabled or disabled in a
                  standard. </p>
                tags:
                  - Batches
                  - Get
                  - Standards
                  - Control
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
            /findings/import:
              POST:
                summary: BatchImportFindings
                description: >-
                  <p>Imports security findings generated by a finding provider
                  into Security Hub. This action is requested by the finding
                  provider to import its findings into Security Hub.</p> <p>
                  <code>BatchImportFindings</code> must be called by one of the
                  following:</p> <ul> <li> <p>The Amazon Web Services account
                  that is associated with a finding if you are using the <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-custom-providers.html#securityhub-custom-providers-bfi-reqs">default
                  product ARN</a> or are a partner sending findings from within
                  a customer's Amazon Web Services account. In these cases, the
                  identifier of the account that you are calling
                  <code>BatchImportFindings</code> from needs to be the same as
                  the <code>AwsAccountId</code> attribute for the finding.</p>
                  </li> <li> <p>An Amazon Web Services account that Security Hub
                  has allow-listed for an official partner integration. In this
                  case, you can call <code>BatchImportFindings</code> from the
                  allow-listed account and send findings from different customer
                  accounts in the same batch.</p> </li> </ul> <p>The maximum
                  allowed size for a finding is 240 Kb. An error is returned for
                  any finding larger than 240 Kb.</p> <p>After a finding is
                  created, <code>BatchImportFindings</code> cannot be used to
                  update the following finding fields and objects, which
                  Security Hub customers use to manage their investigation
                  workflow.</p> <ul> <li> <p> <code>Note</code> </p> </li> <li>
                  <p> <code>UserDefinedFields</code> </p> </li> <li> <p>
                  <code>VerificationState</code> </p> </li> <li> <p>
                  <code>Workflow</code> </p> </li> </ul> <p>Finding providers
                  also should not use <code>BatchImportFindings</code> to update
                  the following attributes.</p> <ul> <li> <p>
                  <code>Confidence</code> </p> </li> <li> <p>
                  <code>Criticality</code> </p> </li> <li> <p>
                  <code>RelatedFindings</code> </p> </li> <li> <p>
                  <code>Severity</code> </p> </li> <li> <p> <code>Types</code>
                  </p> </li> </ul> <p>Instead, finding providers use
                  <code>FindingProviderFields</code> to provide values for these
                  attributes.</p>
                tags:
                  - Batches
                  - Import
                  - Findings
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
            /automationrules/update:
              PATCH:
                summary: BatchUpdateAutomationRules
                description: >-
                  <p> Updates one or more automation rules based on rule Amazon
                  Resource Names (ARNs) and input parameters. </p>
                tags:
                  - Batches
                  - Update
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
            /findings/batchupdate:
              PATCH:
                summary: BatchUpdateFindings
                description: >-
                  <p>Used by Security Hub customers to update information about
                  their investigation into a finding. Requested by administrator
                  accounts or member accounts. Administrator accounts can update
                  findings for their account and their member accounts. Member
                  accounts can update findings for their account.</p> <p>Updates
                  from <code>BatchUpdateFindings</code> do not affect the value
                  of <code>UpdatedAt</code> for a finding.</p> <p>Administrator
                  and member accounts can use <code>BatchUpdateFindings</code>
                  to update the following finding fields and objects.</p> <ul>
                  <li> <p> <code>Confidence</code> </p> </li> <li> <p>
                  <code>Criticality</code> </p> </li> <li> <p> <code>Note</code>
                  </p> </li> <li> <p> <code>RelatedFindings</code> </p> </li>
                  <li> <p> <code>Severity</code> </p> </li> <li> <p>
                  <code>Types</code> </p> </li> <li> <p>
                  <code>UserDefinedFields</code> </p> </li> <li> <p>
                  <code>VerificationState</code> </p> </li> <li> <p>
                  <code>Workflow</code> </p> </li> </ul> <p>You can configure
                  IAM policies to restrict access to fields and field values.
                  For example, you might not want member accounts to be able to
                  suppress findings or change the finding severity. See <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/finding-update-batchupdatefindings.html#batchupdatefindings-configure-access">Configuring
                  access to BatchUpdateFindings</a> in the <i>Security Hub User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Update
                  - Findings
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
            /associations:
              GET:
                summary: ListStandardsControlAssociations
                description: >-
                  <p> Specifies whether a control is currently enabled or
                  disabled in each enabled standard in the calling account. </p>
                tags:
                  - Lists
                  - Standards
                  - Control
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
            /actionTargets:
              POST:
                summary: CreateActionTarget
                description: >-
                  <p>Creates a custom action target in Security Hub.</p> <p>You
                  can use custom actions on findings and insights in Security
                  Hub to trigger target actions in Amazon CloudWatch Events.</p>
                tags:
                  - Create
                  - Actions
                  - Target
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
            /automationrules/create:
              POST:
                summary: CreateAutomationRule
                description: <p> Creates an automation rule based on input parameters. </p>
                tags:
                  - Create
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
            /configurationPolicy/create:
              POST:
                summary: CreateConfigurationPolicy
                description: >-
                  <p> Creates a configuration policy with the defined
                  configuration. Only the Security Hub delegated administrator
                  can invoke this operation from the home Region. </p>
                tags:
                  - Create
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
            /findingAggregator/create:
              POST:
                summary: CreateFindingAggregator
                description: >-
                  <p>Used to enable finding aggregation. Must be called from the
                  aggregation Region.</p> <p>For more details about cross-Region
                  replication, see <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/finding-aggregation.html">Configuring
                  finding aggregation</a> in the <i>Security Hub User Guide</i>.
                  </p>
                tags:
                  - Create
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
            /insights:
              POST:
                summary: CreateInsight
                description: >-
                  <p>Creates a custom insight in Security Hub. An insight is a
                  consolidation of findings that relate to a security issue that
                  requires attention or remediation.</p> <p>To group the related
                  findings in the insight, use the
                  <code>GroupByAttribute</code>.</p>
                tags:
                  - Create
                  - Insight
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
            /members:
              GET:
                summary: ListMembers
                description: >-
                  <p>Lists details about all member accounts for the current
                  Security Hub administrator account.</p> <p>The results include
                  both member accounts that belong to an organization and member
                  accounts that were invited manually.</p>
                tags:
                  - Lists
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
            /invitations/decline:
              POST:
                summary: DeclineInvitations
                description: >-
                  <p>Declines invitations to become a member account.</p> <p>A
                  prospective member account uses this operation to decline an
                  invitation to become a member.</p> <p>This operation is only
                  called by member accounts that aren't part of an organization.
                  Organization accounts don't receive invitations.</p>
                tags:
                  - Decline
                  - Invitations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
            /actionTargets/{ActionTargetArn+}:
              PATCH:
                summary: UpdateActionTarget
                description: >-
                  <p>Updates the name and description of a custom action target
                  in Security Hub.</p>
                tags:
                  - Update
                  - Actions
                  - Target
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
            /configurationPolicy/{Identifier}:
              PATCH:
                summary: UpdateConfigurationPolicy
                description: >-
                  <p> Updates a configuration policy. Only the Security Hub
                  delegated administrator can invoke this operation from the
                  home Region. </p>
                tags:
                  - Update
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
            /findingAggregator/delete/{FindingAggregatorArn+}:
              DELETE:
                summary: DeleteFindingAggregator
                description: >-
                  <p>Deletes a finding aggregator. When you delete the finding
                  aggregator, you stop finding aggregation.</p> <p>When you stop
                  finding aggregation, findings that were already aggregated to
                  the aggregation Region are still visible from the aggregation
                  Region. New findings and finding updates are not aggregated.
                  </p>
                tags:
                  - Delete
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
            /insights/{InsightArn+}:
              PATCH:
                summary: UpdateInsight
                description: >-
                  <p>Updates the Security Hub insight identified by the
                  specified insight ARN.</p>
                tags:
                  - Update
                  - Insight
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /invitations/delete:
              POST:
                summary: DeleteInvitations
                description: >-
                  <p>Deletes invitations received by the Amazon Web Services
                  account to become a member account.</p> <p>A Security Hub
                  administrator account can use this operation to delete
                  invitations sent to one or more member accounts.</p> <p>This
                  operation is only used to delete invitations that are sent to
                  member accounts that aren't part of an organization.
                  Organization accounts don't receive invitations.</p>
                tags:
                  - Delete
                  - Invitations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /members/delete:
              POST:
                summary: DeleteMembers
                description: >-
                  <p>Deletes the specified member accounts from Security
                  Hub.</p> <p>You can invoke this API only to delete accounts
                  that became members through invitation. You can't invoke this
                  API to delete accounts that belong to an Organizations
                  organization.</p>
                tags:
                  - Delete
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /actionTargets/get:
              POST:
                summary: DescribeActionTargets
                description: >-
                  <p>Returns a list of the custom action targets in Security Hub
                  in your account.</p>
                tags:
                  - Describe
                  - Actions
                  - Targets
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /accounts:
              PATCH:
                summary: UpdateSecurityHubConfiguration
                description: <p>Updates configuration options for Security Hub.</p>
                tags:
                  - Update
                  - Security
                  - Hub
                  - Configurations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
            /organization/configuration:
              POST:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the configuration of your organization in Security
                  Hub. Only the Security Hub administrator account can invoke
                  this operation.</p>
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
            /products:
              GET:
                summary: DescribeProducts
                description: >-
                  <p>Returns information about product integrations in Security
                  Hub.</p> <p>You can optionally provide an integration ARN. If
                  you provide an integration ARN, then the results only include
                  that integration.</p> <p>If you do not provide an integration
                  ARN, then the results include all of the available product
                  integrations. </p>
                tags:
                  - Describe
                  - Products
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
            /standards:
              GET:
                summary: DescribeStandards
                description: >-
                  <p>Returns a list of the available standards in Security
                  Hub.</p> <p>For each standard, the results include the
                  standard ARN, the name, and a description. </p>
                tags:
                  - Describe
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
            /standards/controls/{StandardsSubscriptionArn+}:
              GET:
                summary: DescribeStandardsControls
                description: >-
                  <p>Returns a list of security standards controls.</p> <p>For
                  each control, the results include information about whether it
                  is currently enabled, the severity, and a link to remediation
                  information.</p>
                tags:
                  - Describe
                  - Standards
                  - Controls
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
            /productSubscriptions/{ProductSubscriptionArn+}:
              DELETE:
                summary: DisableImportFindingsForProduct
                description: >-
                  <p>Disables the integration of the specified product with
                  Security Hub. After the integration is disabled, findings from
                  that product are no longer sent to Security Hub.</p>
                tags:
                  - Disable
                  - Import
                  - Findings
                  - For
                  - Products
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
            /organization/admin/disable:
              POST:
                summary: DisableOrganizationAdminAccount
                description: >-
                  <p>Disables a Security Hub administrator account. Can only be
                  called by the organization management account.</p>
                tags:
                  - Disable
                  - Organizations
                  - Administrative
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
            /administrator/disassociate:
              POST:
                summary: DisassociateFromAdministratorAccount
                description: >-
                  <p>Disassociates the current Security Hub member account from
                  the associated administrator account.</p> <p>This operation is
                  only used by accounts that are not part of an organization.
                  For organization accounts, only the administrator account can
                  disassociate a member account.</p>
                tags:
                  - Disassociate
                  - From
                  - Administrator
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /master/disassociate:
              POST:
                summary: DisassociateFromMasterAccount
                description: >-
                  <p>This method is deprecated. Instead, use
                  <code>DisassociateFromAdministratorAccount</code>.</p> <p>The
                  Security Hub console continues to use
                  <code>DisassociateFromMasterAccount</code>. It will eventually
                  change to use
                  <code>DisassociateFromAdministratorAccount</code>. Any IAM
                  policies that specifically control access to this function
                  must continue to use
                  <code>DisassociateFromMasterAccount</code>. You should also
                  add <code>DisassociateFromAdministratorAccount</code> to your
                  policies to ensure that the correct permissions are in place
                  after the console begins to use
                  <code>DisassociateFromAdministratorAccount</code>.</p>
                  <p>Disassociates the current Security Hub member account from
                  the associated administrator account.</p> <p>This operation is
                  only used by accounts that are not part of an organization.
                  For organization accounts, only the administrator account can
                  disassociate a member account.</p>
                tags:
                  - Disassociate
                  - From
                  - Master
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /members/disassociate:
              POST:
                summary: DisassociateMembers
                description: >-
                  <p>Disassociates the specified member accounts from the
                  associated administrator account.</p> <p>Can be used to
                  disassociate both accounts that are managed using
                  Organizations and accounts that were invited manually.</p>
                tags:
                  - Disassociate
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /productSubscriptions:
              GET:
                summary: ListEnabledProductsForImport
                description: >-
                  <p>Lists all findings-generating solutions (products) that you
                  are subscribed to receive findings from in Security Hub.</p>
                tags:
                  - Lists
                  - Enabled
                  - Products
                  - For
                  - Import
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /organization/admin/enable:
              POST:
                summary: EnableOrganizationAdminAccount
                description: >-
                  <p>Designates the Security Hub administrator account for an
                  organization. Can only be called by the organization
                  management account.</p>
                tags:
                  - Enable
                  - Organizations
                  - Administrative
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /configurationPolicy/get/{Identifier}:
              GET:
                summary: GetConfigurationPolicy
                description: >-
                  <p> Provides information about a configuration policy. Only
                  the Security Hub delegated administrator can invoke this
                  operation from the home Region. </p>
                tags:
                  - Get
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /configurationPolicyAssociation/get:
              POST:
                summary: GetConfigurationPolicyAssociation
                description: >-
                  <p> Returns the association between a configuration and a
                  target account, organizational unit, or the root. The
                  configuration can be a configuration policy or self-managed
                  behavior. Only the Security Hub delegated administrator can
                  invoke this operation from the home Region. </p>
                tags:
                  - Get
                  - Configurations
                  - Policies
                  - Association
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /standards/get:
              POST:
                summary: GetEnabledStandards
                description: >-
                  <p>Returns a list of the standards that are currently
                  enabled.</p>
                tags:
                  - Get
                  - Enabled
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /findingAggregator/get/{FindingAggregatorArn+}:
              GET:
                summary: GetFindingAggregator
                description: <p>Returns the current finding aggregation configuration.</p>
                tags:
                  - Get
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /findingHistory/get:
              POST:
                summary: GetFindingHistory
                description: >-
                  <p> Returns history for a Security Hub finding in the last 90
                  days. The history includes changes made to any fields in the
                  Amazon Web Services Security Finding Format (ASFF). </p>
                tags:
                  - Get
                  - Findings
                  - History
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /findings:
              PATCH:
                summary: UpdateFindings
                description: >-
                  <p> <code>UpdateFindings</code> is deprecated. Instead of
                  <code>UpdateFindings</code>, use
                  <code>BatchUpdateFindings</code>.</p> <p>Updates the
                  <code>Note</code> and <code>RecordState</code> of the Security
                  Hub-aggregated findings that the filter attributes specify.
                  Any member account that can view the finding also sees the
                  update to the finding.</p>
                tags:
                  - Update
                  - Findings
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /insights/results/{InsightArn+}:
              GET:
                summary: GetInsightResults
                description: >-
                  <p>Lists the results of the Security Hub insight specified by
                  the insight ARN.</p>
                tags:
                  - Get
                  - Insight
                  - Results
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /insights/get:
              POST:
                summary: GetInsights
                description: >-
                  <p>Lists and describes insights for the specified insight
                  ARNs.</p>
                tags:
                  - Get
                  - Insights
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /invitations/count:
              GET:
                summary: GetInvitationsCount
                description: >-
                  <p>Returns the count of all Security Hub membership
                  invitations that were sent to the current member account, not
                  including the currently accepted invitation. </p>
                tags:
                  - Get
                  - Invitations
                  - Count
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
            /members/get:
              POST:
                summary: GetMembers
                description: >-
                  <p>Returns the details for the Security Hub member accounts
                  for the specified account IDs.</p> <p>An administrator account
                  can be either the delegated Security Hub administrator account
                  for an organization or an administrator account that enabled
                  Security Hub manually.</p> <p>The results include both member
                  accounts that are managed using Organizations and accounts
                  that were invited manually.</p>
                tags:
                  - Get
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
            /securityControl/definition:
              GET:
                summary: GetSecurityControlDefinition
                description: >-
                  <p> Retrieves the definition of a security control. The
                  definition includes the control title, description, Region
                  availability, parameter definitions, and other details. </p>
                tags:
                  - Get
                  - Security
                  - Control
                  - Definitions
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
            /members/invite:
              POST:
                summary: InviteMembers
                description: >-
                  <p>Invites other Amazon Web Services accounts to become member
                  accounts for the Security Hub administrator account that the
                  invitation is sent from.</p> <p>This operation is only used to
                  invite accounts that do not belong to an organization.
                  Organization accounts do not receive invitations.</p>
                  <p>Before you can use this action to invite a member, you must
                  first use the <code>CreateMembers</code> action to create the
                  member account in Security Hub.</p> <p>When the account owner
                  enables Security Hub and accepts the invitation to become a
                  member account, the administrator account can view the
                  findings generated from the member account.</p>
                tags:
                  - Invite
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
            /automationrules/list:
              GET:
                summary: ListAutomationRules
                description: >-
                  <p> A list of automation rules and their metadata for the
                  calling account. </p>
                tags:
                  - Lists
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /configurationPolicy/list:
              GET:
                summary: ListConfigurationPolicies
                description: >-
                  <p> Lists the configuration policies that the Security Hub
                  delegated administrator has created for your organization.
                  Only the delegated administrator can invoke this operation
                  from the home Region. </p>
                tags:
                  - Lists
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /configurationPolicyAssociation/list:
              POST:
                summary: ListConfigurationPolicyAssociations
                description: >-
                  <p> Provides information about the associations for your
                  configuration policies and self-managed behavior. Only the
                  Security Hub delegated administrator can invoke this operation
                  from the home Region. </p>
                tags:
                  - Lists
                  - Configurations
                  - Policies
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /findingAggregator/list:
              GET:
                summary: ListFindingAggregators
                description: >-
                  <p>If finding aggregation is enabled, then
                  <code>ListFindingAggregators</code> returns the ARN of the
                  finding aggregator. You can run this operation from any
                  Region.</p>
                tags:
                  - Lists
                  - Findings
                  - Aggregators
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /invitations:
              GET:
                summary: ListInvitations
                description: >-
                  <p>Lists all Security Hub membership invitations that were
                  sent to the current Amazon Web Services account.</p> <p>This
                  operation is only used by accounts that are managed by
                  invitation. Accounts that are managed using the integration
                  with Organizations do not receive invitations.</p>
                tags:
                  - Lists
                  - Invitations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /organization/admin:
              GET:
                summary: ListOrganizationAdminAccounts
                description: >-
                  <p>Lists the Security Hub administrator accounts. Can only be
                  called by the organization management account.</p>
                tags:
                  - Lists
                  - Organizations
                  - Administrative
                  - Accounts
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /securityControls/definitions:
              GET:
                summary: ListSecurityControlDefinitions
                description: >-
                  <p> Lists all of the security controls that apply to a
                  specified standard. </p>
                tags:
                  - Lists
                  - Security
                  - Control
                  - Definitions
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
            /configurationPolicyAssociation/associate:
              POST:
                summary: StartConfigurationPolicyAssociation
                description: >-
                  <p> Associates a target account, organizational unit, or the
                  root with a specified configuration. The target can be
                  associated with a configuration policy or self-managed
                  behavior. Only the Security Hub delegated administrator can
                  invoke this operation from the home Region. </p>
                tags:
                  - Start
                  - Configurations
                  - Policies
                  - Association
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /configurationPolicyAssociation/disassociate:
              POST:
                summary: StartConfigurationPolicyDisassociation
                description: >-
                  <p> Disassociates a target account, organizational unit, or
                  the root from a specified configuration. When you disassociate
                  a configuration from its target, the target inherits the
                  configuration of the closest parent. If there’s no
                  configuration to inherit, the target retains its settings but
                  becomes a self-managed account. A target can be disassociated
                  from a configuration policy or self-managed behavior. Only the
                  Security Hub delegated administrator can invoke this operation
                  from the home Region. </p>
                tags:
                  - Start
                  - Configurations
                  - Policies
                  - Disassociation
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /findingAggregator/update:
              PATCH:
                summary: UpdateFindingAggregator
                description: >-
                  <p>Updates the finding aggregation configuration. Used to
                  update the Region linking mode and the list of included or
                  excluded Regions. You cannot use
                  <code>UpdateFindingAggregator</code> to change the aggregation
                  Region.</p> <p>You must run
                  <code>UpdateFindingAggregator</code> from the current
                  aggregation Region. </p>
                tags:
                  - Update
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /securityControl/update:
              PATCH:
                summary: UpdateSecurityControl
                description: <p> Updates the properties of a security control. </p>
                tags:
                  - Update
                  - Security
                  - Control
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /standards/control/{StandardsControlArn+}:
              PATCH:
                summary: UpdateStandardsControl
                description: >-
                  <p>Used to control whether an individual security standard
                  control is enabled or dis
                tags:
                  - Update
                  - Standards
                  - Control
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associa
    overlays:
      - type: APIs.io Search
        url: overlays/securityhub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/securityhub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:securityhub
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---