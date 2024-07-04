---
name: Assessments
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/assessments.png
url: https://example.com/apis/assessments.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Assessments
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Requests
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
                  - Integri
    overlays:
      - type: APIs.io Search
        url: overlays/auditmanager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/auditmanager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:auditmanager
  - name: inspector
    description: >-
      <fullname>Amazon Inspector</fullname> <p>Amazon Inspector enables you to
      analyze the behavior of your AWS resources and to identify potential
      security issues. For more information, see <a
      href="https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html">
      Amazon Inspector User Guide</a>.</p>
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
            title: inspector
          paths:
            /:
              POST:
                summary: UpdateAssessmentTarget
                description: >-
                  <p>Updates the assessment target that is specified by the ARN
                  of the assessment target.</p> <p>If resourceGroupArn is not
                  specified, all EC2 instances in the current AWS account and
                  region are included in the assessment t
                tags:
                  - Update
                  - Assessments
                  - Targ
    overlays:
      - type: APIs.io Search
        url: overlays/inspector-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/inspector-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:inspector
  - name: migrationhubstrategy
    description: >-
      <p><fullname>Migration Hub Strategy Recommendations</fullname> <p>This API
      reference provides descriptions, syntax, and other details about each of
      the actions and data types for Migration Hub Strategy Recommendations
      (Strategy Recommendations). The topic for each action shows the API
      request parameters and the response. Alternatively, you can use one of the
      AWS SDKs to access an API that is tailored to the programming language or
      platform that you're using. For more information, see <a
      href="http://aws.amazon.com/tools/#SDKs">AWS SDKs</a>.</p></p>
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
            title: migrationhubstrategy
          paths:
            /get-applicationcomponent-details/{applicationComponentId}:
              GET:
                summary: GetApplicationComponentDetails
                description: <p> Retrieves details about an application component. </p>
                tags:
                  - Get
                  - Applications
                  - Components
                  - Details
                  - Components
                  - Identifiers
            /get-applicationcomponent-strategies/{applicationComponentId}:
              GET:
                summary: GetApplicationComponentStrategies
                description: >-
                  <p> Retrieves a list of all the recommended strategies and
                  tools for an application component running on a server. </p>
                tags:
                  - Get
                  - Applications
                  - Components
                  - Strategies
                  - Components
                  - Identifiers
            /get-assessment/{id}:
              GET:
                summary: GetAssessment
                description: <p> Retrieves the status of an on-going assessment. </p>
                tags:
                  - Get
                  - Assessments
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
            /get-import-file-task/{id}:
              GET:
                summary: GetImportFileTask
                description: <p> Retrieves the details about a specific import task. </p>
                tags:
                  - Get
                  - Import
                  - File
                  - Tasks
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
            /get-latest-assessment-id:
              GET:
                summary: GetLatestAssessmentId
                description: <p>Retrieve the latest ID of a specific assessment task.</p>
                tags:
                  - Get
                  - Latest
                  - Assessments
                  - Identifiers
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
            /get-portfolio-preferences:
              GET:
                summary: GetPortfolioPreferences
                description: >-
                  <p> Retrieves your migration and modernization preferences.
                  </p>
                tags:
                  - Get
                  - Portfolio
                  - Preferences
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
            /get-portfolio-summary:
              GET:
                summary: GetPortfolioSummary
                description: >-
                  <p> Retrieves overall summary including the number of servers
                  to rehost and the overall number of anti-patterns. </p>
                tags:
                  - Get
                  - Portfolio
                  - Summaries
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
            /get-recommendation-report-details/{id}:
              GET:
                summary: GetRecommendationReportDetails
                description: >-
                  <p> Retrieves detailed information about the specified
                  recommendation report. </p>
                tags:
                  - Get
                  - Recommendations
                  - Reports
                  - Details
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
            /get-server-details/{serverId}:
              GET:
                summary: GetServerDetails
                description: >-
                  <p> Retrieves detailed information about a specified server.
                  </p>
                tags:
                  - Get
                  - Server
                  - Details
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
            /get-server-strategies/{serverId}:
              GET:
                summary: GetServerStrategies
                description: >-
                  <p> Retrieves recommended strategies and tools for the
                  specified server. </p>
                tags:
                  - Get
                  - Server
                  - Strategies
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
            /list-analyzable-servers:
              POST:
                summary: ListAnalyzableServers
                description: >-
                  <p>Retrieves a list of all the servers fetched from customer
                  vCenter using Strategy Recommendation Collector.</p>
                tags:
                  - Lists
                  - Analyzable
                  - Servers
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
            /list-applicationcomponents:
              POST:
                summary: ListApplicationComponents
                description: >-
                  <p> Retrieves a list of all the application components
                  (processes). </p>
                tags:
                  - Lists
                  - Applications
                  - Components
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
            /list-collectors:
              GET:
                summary: ListCollectors
                description: <p> Retrieves a list of all the installed collectors. </p>
                tags:
                  - Lists
                  - Collectors
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
            /list-import-file-task:
              GET:
                summary: ListImportFileTask
                description: <p> Retrieves a list of all the imports performed. </p>
                tags:
                  - Lists
                  - Import
                  - File
                  - Tasks
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
            /list-servers:
              POST:
                summary: ListServers
                description: <p> Returns a list of all the servers. </p>
                tags:
                  - Lists
                  - Servers
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
            /put-portfolio-preferences:
              POST:
                summary: PutPortfolioPreferences
                description: >-
                  <p> Saves the specified migration and modernization
                  preferences. </p>
                tags:
                  - Put
                  - Portfolio
                  - Preferences
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
            /start-assessment:
              POST:
                summary: StartAssessment
                description: <p> Starts the assessment of an on-premises environment. </p>
                tags:
                  - Start
                  - Assessments
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
            /start-import-file-task:
              POST:
                summary: StartImportFileTask
                description: <p> Starts a file import. </p>
                tags:
                  - Start
                  - Import
                  - File
                  - Tasks
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
            /start-recommendation-report-generation:
              POST:
                summary: StartRecommendationReportGeneration
                description: <p> Starts generating a recommendation report. </p>
                tags:
                  - Start
                  - Recommendations
                  - Reports
                  - Generation
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
            /stop-assessment:
              POST:
                summary: StopAssessment
                description: <p> Stops the assessment of an on-premises environment. </p>
                tags:
                  - Stop
                  - Assessments
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
                  - Stop
            /update-applicationcomponent-config/:
              POST:
                summary: UpdateApplicationComponentConfig
                description: >-
                  <p> Updates the configuration of an application component.
                  </p>
                tags:
                  - Update
                  - Applications
                  - Components
                  - Configurations
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
                  - Stop
                  - Update
                  - Application Components
                  - Configurations
            /update-server-config/:
              POST:
                summary: UpdateServerConfig
                description: <p> Updates the configuration of the specified s
                tags:
                  - Update
                  - Server
                  - Configurations
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
                  - Stop
                  - Update
                  - Application Components
                  - Configurations
                  - Serv
    overlays:
      - type: APIs.io Search
        url: overlays/migrationhubstrategy-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/migrationhubstrategy-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:migrationhubstrategy
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