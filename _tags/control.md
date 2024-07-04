---
name: Control
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/control.png
url: https://example.com/apis/control.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Control
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
  - name: pca-connector-ad
    description: >-
      <p>Amazon Web Services Private CA Connector for Active Directory creates a
      connector between Amazon Web Services Private CA and Active Directory (AD)
      that enables you to provision security certificates for AD signed by a
      private CA that you own. For more information, see <a
      href="https://docs.aws.amazon.com/privateca/latest/userguide/ad-connector.html">Amazon
      Web Services Private CA Connector for Active Directory</a>.</p>
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
            title: pca-connector-ad
          paths:
            /connectors:
              GET:
                summary: ListConnectors
                description: >-
                  <p>Lists the connectors that you created by using the <a
                  href="https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector">https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector</a>
                  action.</p>
                tags:
                  - Lists
                  - Connectors
                  - Connectors
            /directoryRegistrations:
              GET:
                summary: ListDirectoryRegistrations
                description: >-
                  <p>Lists the directory registrations that you created by using
                  the <a
                  href="https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateDirectoryRegistration">https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateDirectoryRegistration</a>
                  action.</p>
                tags:
                  - Lists
                  - Directory
                  - Registrations
                  - Connectors
                  - Registrations
            /directoryRegistrations/{DirectoryRegistrationArn}/servicePrincipalNames/{ConnectorArn}:
              GET:
                summary: GetServicePrincipalName
                description: >-
                  <p>Lists the service principal name that the connector uses to
                  authenticate with Active Directory.</p>
                tags:
                  - Get
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
            /templates:
              GET:
                summary: ListTemplates
                description: >-
                  <p>Lists the templates, if any, that are associated with a
                  connector.</p>
                tags:
                  - Lists
                  - Templates
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
            /templates/{TemplateArn}/accessControlEntries:
              GET:
                summary: ListTemplateGroupAccessControlEntries
                description: <p>Lists group access control entries you created. </p>
                tags:
                  - Lists
                  - Templates
                  - Group
                  - Access
                  - Control
                  - Entries
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /connectors/{ConnectorArn}:
              GET:
                summary: GetConnector
                description: >-
                  <p>Lists information about your connector. You specify the
                  connector on input by its ARN (Amazon Resource Name). </p>
                tags:
                  - Get
                  - Connectors
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /directoryRegistrations/{DirectoryRegistrationArn}:
              GET:
                summary: GetDirectoryRegistration
                description: >-
                  <p>A structure that contains information about your directory
                  registration.</p>
                tags:
                  - Get
                  - Directory
                  - Registrations
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /templates/{TemplateArn}:
              PATCH:
                summary: UpdateTemplate
                description: >-
                  <p>Update template configuration to define the information
                  included in certificates.</p>
                tags:
                  - Update
                  - Templates
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /templates/{TemplateArn}/accessControlEntries/{GroupSecurityIdentifier}:
              PATCH:
                summary: UpdateTemplateGroupAccessControlEntry
                description: >-
                  <p>Update a group access control entry you created using <a
                  href="https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateTemplateGroupAccessControlEntry.html">CreateTemplateGroupAccessControlEntry</a>.
                  </p>
                tags:
                  - Update
                  - Templates
                  - Group
                  - Access
                  - Control
                  - Entry
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
                  - Group
                  - Security
                  - Identifiers
            /directoryRegistrations/{DirectoryRegistrationArn}/servicePrincipalNames:
              GET:
                summary: ListServicePrincipalNames
                description: >-
                  <p>Lists the service principal names that the connector uses
                  to authenticate with Active Directory.</p>
                tags:
                  - Lists
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
                  - Group
                  - Security
                  - Identifiers
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from your res
                tags:
                  - Untag
                  - Resources
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
                  - Group
                  - Security
                  - Identifiers
                  - Resour
    overlays:
      - type: APIs.io Search
        url: overlays/pca-connector-ad-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pca-connector-ad-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pca-connector-ad
  - name: route53-recovery-cluster
    description: >-
      <p>Welcome to the Routing Control (Recovery Cluster) API Reference Guide
      for Amazon Route 53 Application Recovery Controller.</p> <p>With Route 53
      ARC, you can use routing control with extreme reliability to recover
      applications by rerouting traffic across Availability Zones or Amazon Web
      Services Regions. Routing controls are simple on/off switches hosted on a
      highly available cluster in Route 53 ARC. A cluster provides a set of five
      redundant Regional endpoints against which you can run API calls to get or
      update the state of routing controls. To implement failover, you set one
      routing control to ON and another one to OFF, to reroute traffic from one
      Availability Zone or Amazon Web Services Region to another. </p> <p> <i>Be
      aware that you must specify a Regional endpoint for a cluster when you
      work with API cluster operations to get or update routing control states
      in Route 53 ARC.</i> In addition, you must specify the US West (Oregon)
      Region for Route 53 ARC API calls. For example, use the parameter
      <code>--region us-west-2</code> with AWS CLI commands. For more
      information, see <a
      href="https://docs.aws.amazon.com/r53recovery/latest/dg/routing-control.update.api.html">
      Get and update routing control states using the API</a> in the Amazon
      Route 53 Application Recovery Controller Developer Guide.</p> <p>This API
      guide includes information about the API operations for how to get and
      update routing control states in Route 53 ARC. To work with routing
      control in Route 53 ARC, you must first create the required components
      (clusters, control panels, and routing controls) using the recovery
      cluster configuration API.</p> <p>For more information about working with
      routing control in Route 53 ARC, see the following:</p> <ul> <li>
      <p>Create clusters, control panels, and routing controls by using API
      operations. For more information, see the <a
      href="https://docs.aws.amazon.com/recovery-cluster/latest/api/">Recovery
      Control Configuration API Reference Guide for Amazon Route 53 Application
      Recovery Controller</a>.</p> </li> <li> <p>Learn about the components in
      recovery control, including clusters, routing controls, and control
      panels, and how to work with Route 53 ARC in the Amazon Web Services
      console. For more information, see <a
      href="https://docs.aws.amazon.com/r53recovery/latest/dg/introduction-components.html#introduction-components-routing">
      Recovery control components</a> in the Amazon Route 53 Application
      Recovery Controller Developer Guide.</p> </li> <li> <p>Route 53 ARC also
      provides readiness checks that continually audit resources to help make
      sure that your applications are scaled and ready to handle failover
      traffic. For more information about the related API operations, see the <a
      href="https://docs.aws.amazon.com/recovery-readiness/latest/api/">Recovery
      Readiness API Reference Guide for Amazon Route 53 Application Recovery
      Controller</a>.</p> </li> <li> <p>For more information about creating
      resilient applications and preparing for recovery readiness with Route 53
      ARC, see the <a
      href="https://docs.aws.amazon.com/r53recovery/latest/dg/">Amazon Route 53
      Application Recovery Controller Developer Guide</a>.</p> </li> </ul>
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
            title: route53-recovery-cluster
          paths:
            /:
              POST:
                summary: UpdateRoutingControlStates
                description: >-
                  <p>Set multiple routing control states. You can set the value
                  for each state to be ON or OFF. When the state is ON, traffic
                  flows to a cell. When it's OFF, traffic does not flow.</p>
                  <p>With Route 53 ARC, you can add safety rules for routing
                  controls, which are safeguards for routing control state
                  updates that help prevent unexpected outcomes, like fail open
                  traffic routing. However, there are scenarios when you might
                  want to bypass the routing control safeguards that are
                  enforced with safety rules that you've configured. For
                  example, you might want to fail over quickly for disaster
                  recovery, and one or more safety rules might be unexpectedly
                  preventing you from updating a routing control state to
                  reroute traffic. In a "break glass" scenario like this, you
                  can override one or more safety rules to change a routing
                  control state and fail over your application.</p> <p>The
                  <code>SafetyRulesToOverride</code> property enables you
                  override one or more safety rules and update routing control
                  states. For more information, see <a
                  href="https://docs.aws.amazon.com/r53recovery/latest/dg/routing-control.override-safety-rule.html">
                  Override safety rules to reroute traffic</a> in the Amazon
                  Route 53 Application Recovery Controller Developer Guide.</p>
                  <p> <i>You must specify Regional endpoints when you work with
                  API cluster operations to get or update routing control states
                  in Route 53 ARC.</i> </p> <p>To see a code example for getting
                  a routing control state, including accessing Regional cluster
                  endpoints in sequence, see <a
                  href="https://docs.aws.amazon.com/r53recovery/latest/dg/service_code_examples_actions.html">API
                  examples</a> in the Amazon Route 53 Application Recovery
                  Controller Developer Guide.</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/r53recovery/latest/dg/routing-control.update.html">
                  Viewing and updating routing control states</a> </p> </li>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/r53recovery/latest/dg/routing-control.html">Working
                  with routing controls overall</a> </p> <
                tags:
                  - Update
                  - Routing
                  - Control
                  - Stat
    overlays:
      - type: APIs.io Search
        url: overlays/route53-recovery-cluster-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-recovery-cluster-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53-recovery-cluster
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
  - name: support-app
    description: >-
      <p><fullname>Amazon Web Services Support App in Slack</fullname> <p>You
      can use the Amazon Web Services Support App in Slack API to manage your
      support cases in Slack for your Amazon Web Services account. After you
      configure your Slack workspace and channel with the Amazon Web Services
      Support App, you can perform the following tasks directly in your Slack
      channel:</p> <ul> <li> <p>Create, search, update, and resolve your support
      cases</p> </li> <li> <p>Request service quota increases for your
      account</p> </li> <li> <p>Invite Amazon Web Services Support agents to
      your channel so that you can chat directly about your support cases</p>
      </li> </ul> <p>For more information about how to perform these actions in
      Slack, see the following documentation in the <i>Amazon Web Services
      Support User Guide</i>:</p> <ul> <li> <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/aws-support-app-for-slack.html">Amazon
      Web Services Support App in Slack</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/joining-a-live-chat-session.html">Joining
      a live chat session with Amazon Web Services Support</a> </p> </li> <li>
      <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/service-quota-increase.html">Requesting
      service quota increases</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/support-app-commands.html">Amazon
      Web Services Support App commands in Slack</a> </p> </li> </ul> <p>You can
      also use the Amazon Web Services Management Console instead of the Amazon
      Web Services Support App API to manage your Slack configurations. For more
      information, see <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/authorize-slack-workspace.html">Authorize
      a Slack workspace to enable the Amazon Web Services Support App</a>.</p>
      <note> <ul> <li> <p>You must have a Business or Enterprise Support plan to
      use the Amazon Web Services Support App API. </p> </li> <li> <p>For more
      information about the Amazon Web Services Support App endpoints, see the
      <a
      href="https://docs.aws.amazon.com/general/latest/gr/awssupport.html#awssupport_app_region">Amazon
      Web Services Support App in Slack endpoints</a> in the <i>Amazon Web
      Services General Reference</i>.</p> </li> </ul> </note></p>
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
            title: support-app
          paths:
            /control/create-slack-channel-configuration:
              POST:
                summary: CreateSlackChannelConfiguration
                description: >-
                  <p>Creates a Slack channel configuration for your Amazon Web
                  Services account.</p> <note> <ul> <li> <p>You can add up to 5
                  Slack workspaces for your account.</p> </li> <li> <p>You can
                  add up to 20 Slack channels for your account.</p> </li> </ul>
                  </note> <p>A Slack channel can have up to 100 Amazon Web
                  Services accounts. This means that only 100 accounts can add
                  the same Slack channel to the Amazon Web Services Support App.
                  We recommend that you only add the accounts that you need to
                  manage support cases for your organization. This can reduce
                  the notifications about case updates that you receive in the
                  Slack channel.</p> <note> <p>We recommend that you choose a
                  private Slack channel so that only members in that channel
                  have read and write access to your support cases. Anyone in
                  your Slack channel can create, update, or resolve support
                  cases for your account. Users require an invitation to join
                  private channels. </p> </note>
                tags:
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
            /control/delete-account-alias:
              POST:
                summary: DeleteAccountAlias
                description: >-
                  <p>Deletes an alias for an Amazon Web Services account ID. The
                  alias appears in the Amazon Web Services Support App page of
                  the Amazon Web Services Support Center. The alias also appears
                  in Slack messages from the Amazon Web Services Support
                  App.</p>
                tags:
                  - Delete
                  - Account
                  - Alias
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
            /control/delete-slack-channel-configuration:
              POST:
                summary: DeleteSlackChannelConfiguration
                description: >-
                  <p>Deletes a Slack channel configuration from your Amazon Web
                  Services account. This operation doesn't delete your Slack
                  channel.</p>
                tags:
                  - Delete
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
            /control/delete-slack-workspace-configuration:
              POST:
                summary: DeleteSlackWorkspaceConfiguration
                description: >-
                  <p>Deletes a Slack workspace configuration from your Amazon
                  Web Services account. This operation doesn't delete your Slack
                  workspace.</p>
                tags:
                  - Delete
                  - Slack
                  - Workspaces
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
            /control/get-account-alias:
              POST:
                summary: GetAccountAlias
                description: >-
                  <p>Retrieves the alias from an Amazon Web Services account ID.
                  The alias appears in the Amazon Web Services Support App page
                  of the Amazon Web Services Support Center. The alias also
                  appears in Slack messages from the Amazon Web Services Support
                  App.</p>
                tags:
                  - Get
                  - Account
                  - Alias
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
            /control/list-slack-channel-configurations:
              POST:
                summary: ListSlackChannelConfigurations
                description: >-
                  <p>Lists the Slack channel configurations for an Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
            /control/list-slack-workspace-configurations:
              POST:
                summary: ListSlackWorkspaceConfigurations
                description: >-
                  <p>Lists the Slack workspace configurations for an Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Slack
                  - Workspaces
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
            /control/put-account-alias:
              POST:
                summary: PutAccountAlias
                description: >-
                  <p>Creates or updates an individual alias for each Amazon Web
                  Services account ID. The alias appears in the Amazon Web
                  Services Support App page of the Amazon Web Services Support
                  Center. The alias also appears in Slack messages from the
                  Amazon Web Services Support App.</p>
                tags:
                  - Put
                  - Account
                  - Alias
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
                  - Put
            /control/register-slack-workspace-for-organization:
              POST:
                summary: RegisterSlackWorkspaceForOrganization
                description: >-
                  <p>Registers a Slack workspace for your Amazon Web Services
                  account. To call this API, your account must be part of an
                  organization in Organizations.</p> <p>If you're the
                  <i>management account</i> and you want to register Slack
                  workspaces for your organization, you must complete the
                  following tasks:</p> <ol> <li> <p>Sign in to the <a
                  href="https://console.aws.amazon.com/support/app">Amazon Web
                  Services Support Center</a> and authorize the Slack workspaces
                  where you want your organization to have access to. See <a
                  href="https://docs.aws.amazon.com/awssupport/latest/user/authorize-slack-workspace.html">Authorize
                  a Slack workspace</a> in the <i>Amazon Web Services Support
                  User Guide</i>.</p> </li> <li> <p>Call the
                  <code>RegisterSlackWorkspaceForOrganization</code> API to
                  authorize each Slack workspace for the organization.</p> </li>
                  </ol> <p>After the management account authorizes the Slack
                  workspace, member accounts can call this API to authorize the
                  same Slack workspace for their individual accounts. Member
                  accounts don't need to authorize the Slack workspace manually
                  through the <a
                  href="https://console.aws.amazon.com/support/app">Amazon Web
                  Services Support Center</a>.</p> <p>To use the Amazon Web
                  Services Support App, each account must then complete the
                  following tasks:</p> <ul> <li> <p>Create an Identity and
                  Access Management (IAM) role with the required permission. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/awssupport/latest/user/support-app-permissions.html">Managing
                  access to the Amazon Web Services Support App</a>.</p> </li>
                  <li> <p>Configure a Slack channel to use the Amazon Web
                  Services Support App for support cases for that account. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/awssupport/latest/user/add-your-slack-channel.html">Configuring
                  a Slack channel</a>.</p> </li> </ul>
                tags:
                  - Register
                  - Slack
                  - Workspaces
                  - For
                  - Organizations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
                  - Put
                  - Register
                  - For
                  - Organizations
            /control/update-slack-channel-configuration:
              POST:
                summary: UpdateSlackChannelConfiguration
                description: >-
                  <p>Updates the configuration for a Slack channel, such as case
                  update notifica
                tags:
                  - Update
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
                  - Put
                  - Register
                  - For
                  - Organizations
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/support-app-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/support-app-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:support-app
  - name: FactSet Entity API
    description: ' FactSet’s Entity API provides access to FactSet’s complete security and entity level symbology, comprehensive entity reference data, and all of the necessary relationships and connections to create a foundation that tightly correlates disparate sources o'
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-entity-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-entity-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-entity-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-entity-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-entity-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-entity-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Entity API
          tags:
            - name: Entity Reference
              description: >-
                Retrieve Entity Reference information for a list of securities,
                such as Parent Equity and Business Descriptions.
            - name: Entity Securities
              description: >-
                Retrieve the related equity or fixed income securities for a
                given list of ids
            - name: Entity Structure
              description: >-
                Retrieve the Entities corporate structure, its subsidiaries and
                related entity ids.
            - name: Entity Reference Chinese
            - name: Historical Credit Parent
          paths:
            /factset-entity/v1/entity-references:
              get:
                summary: Returns an entity reference profiles for an individual entity
                description: >
                  Returns an Entity reference profile for the requested Entity
                  Id(s). Data points include - Ultimate Parent Id, Credit Parent
                  Id, Headquarters location details, Website URL, and Business
                  Description.
                tags:
                  - Returns
                  - An
                  - Entity
                  - Reference
                  - Profiles
                  - For
                  - Individual
                  - Factset
                  - Entity
                  - V1
                  - References
              post:
                summary: Returns an entity reference data for a list of ids.
                description: >
                  Returns an entity reference object for the requested entity
                  ids. Data points include - ultimate parent id, headquarters
                  location details, credit parent id, website, and business
                  description.
                tags:
                  - Returns
                  - An
                  - Entity
                  - Reference
                  - Data
                  - For
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Entity
                  - V1
                  - References
            /factset-entity/v1/entity-securities:
              get:
                summary: >-
                  Returns all Equity Exchange Listings and all debt instruments
                  issued for the requested entity.
                description: >
                  Returns all Equity Exchange Listings (ticker-exchange) and all
                  debt instruments (cusips) issued for the requested entity.
                tags:
                  - Returns
                  - All
                  - Equity
                  - Exchange
                  - Listings
                  - And
                  - Debt
                  - Instruments
                  - Issued
                  - For
                  - The
                  - Requested
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
              post:
                summary: >-
                  Returns all Equity Exchange Listings and all debt instruments
                  issued for the requested entity.
                description: >
                  Returns all Equity Exchange Listings (ticker-exchange) and all
                  debt instruments (cusips) issued for the requested entity.
                tags:
                  - Returns
                  - All
                  - Equity
                  - Exchange
                  - Listings
                  - And
                  - Debt
                  - Instruments
                  - Issued
                  - For
                  - The
                  - Requested
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
            /factset-entity/v1/entity-structures:
              get:
                summary: >-
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                description: >
                  Returns all active or inactive entities below the requested
                  entity id.
                tags:
                  - Returns
                  - All
                  - Active
                  - Or
                  - Inactive
                  - Entities
                  - And
                  - Respective
                  - Levels
                  - Below
                  - The
                  - Requested
                  - Entity
                  - Id.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
              post:
                summary: >-
                  Returns all active or inactive entities below the requested
                  entity id.
                description: >
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                tags:
                  - Returns
                  - All
                  - Active
                  - Or
                  - Inactive
                  - Entities
                  - Below
                  - The
                  - Requested
                  - Entity
                  - Id.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
            /factset-entity/v1/ultimate-entity-structures:
              get:
                summary: >-
                  Returns the full ultimate parent entity hiearachy. Control
                  levels and active status of underlying entities.
                description: >
                  Returns full ultimate entity structure including ultimate
                  parent and all subordinates. Will accept entity from any level
                  of entity structure or active vs. inactive status of entity.
                tags:
                  - Returns
                  - The
                  - Full
                  - Ultimate
                  - Parent
                  - Entity
                  - Hiearachy.
                  - Control
                  - Levels
                  - And
                  - Active
                  - Status
                  - Of
                  - Underlying
                  - Entities.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
              post:
                summary: >-
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                description: >
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                tags:
                  - Returns
                  - All
                  - Active
                  - Or
                  - Inactive
                  - Entities
                  - And
                  - Respective
                  - Levels
                  - Below
                  - The
                  - Requested
                  - Entity
                  - Id.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
            /factset-entity/v1/entity-reference-chi:
              get:
                summary: >-
                  Returns entity reference data in Chinese for an individual
                  entity.
                description: >
                  Returns entity reference data in Chinese for the requested
                  Id(s). Data points include Business Description and Entity
                  Name in both simplified and traditional Chinese.
                tags:
                  - Returns
                  - Entity
                  - Reference
                  - Data
                  - In
                  - Chinese
                  - For
                  - An
                  - Individual
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
              post:
                summary: >-
                  Returns entity reference data in Chinese for an individual
                  entity.
                description: >
                  Returns entity reference data in Chinese for the requested
                  Id(s). Data points include Business Description and Entity
                  Name in both simplified and traditional Chinese.
                tags:
                  - Returns
                  - Entity
                  - Reference
                  - Data
                  - In
                  - Chinese
                  - For
                  - An
                  - Individual
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
            /factset-entity/v1/hist-credit-parent:
              get:
                summary: Returns historical credit parents for the requested id(s).
                description: >
                  Returns the credit parent for requested fixed income ids.
                  Point in time credit parent retrieval is

                  also available if an asOfDate is provided. The full credit
                  parent history of a security is returned if

                  no asOfDate is provided.


                  This endpoint uses a seven day calendar to account for changes
                  that occur on all seven days of the week.
                tags:
                  - Returns
                  - Historical
                  - Credit
                  - Parents
                  - For
                  - The
                  - Requested
                  - Id(s).
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
                  - Hist
                  - Credit
                  - Parent
              post:
                summary: Returns historical credit parents for the requested id(s).
                description: >
                  Returns the credit parent for requested fixed income ids.
                  Point in time credit parent retrieval is

                  also available if an asOfDate is provided. The full credit
                  parent history of a security is returned if

                  no asOfDate is provided.


                  This endpoint uses a seven day calendar to account for changes
                  that occur on all seven days of the week.
                tags:
                  - Returns
                  - Historical
                  - Credit
                  - Parents
                  - For
                  - The
                  - Requested
                  - Id(s).
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
                  - Hist
                  - Credit
                  - Pare
    overlays:
      - type: APIs.io Search
        url: overlays/entity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/entity-openapi-api-evangelist-ratings.yml
    aid: factset:factset-entity-api
  - aid: twilio:twilio-trunking-api
    name: Twilio Trunking API
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
            title: Twilio - Trunking
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Trunks/{TrunkSid}/CredentialLists/{Sid}:
              description: List of credentials for accessing a trunk
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
              delete:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
            /v1/Trunks/{TrunkSid}/CredentialLists:
              description: List of credentials for accessing a trunk
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
            /v1/Trunks/{TrunkSid}/IpAccessControlLists/{Sid}:
              description: List of IP addresses for accessing a trunk
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
              delete:
                description: Remove an associated IP Access Control List from a Trunk
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
            /v1/Trunks/{TrunkSid}/IpAccessControlLists:
              description: List of IP addresses for accessing a trunk
              post:
                description: Associate an IP Access Control List with a Trunk
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
              get:
                description: List all IP Access Control Lists for a Trunk
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
            /v1/Trunks/{TrunkSid}/OriginationUrls/{Sid}:
              description: >-
                Network element entry points into your communications
                infrastructure
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
              delete:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
            /v1/Trunks/{TrunkSid}/OriginationUrls:
              description: >-
                Network element entry points into your communications
                infrastructure
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
            /v1/Trunks/{TrunkSid}/PhoneNumbers/{Sid}:
              description: Phone numbers associated with trunks
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
              delete:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
            /v1/Trunks/{TrunkSid}/PhoneNumbers:
              description: Phone numbers associated with trunks
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
            /v1/Trunks/{TrunkSid}/Recording:
              description: Recording settings for a trunk
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
            /v1/Trunks/{Sid}:
              description: Represents a SIP trunk
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
              delete:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
            /v1/Trunks:
              description: Represents a SIP trunk
              post:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
              get:
                description: ''
                tags:
                  - Trunks
                  - Trunk
                  - Sid
                  - Credential
                  - Lists
                  - Ip
                  - Access
                  - Control
                  - Origination
                  - Urls
                  - Phone
                  - Numbers
                  - Recording
          tags:
            - name: TrunkingV1CredentialList
            - name: TrunkingV1IpAccessControlList
            - name: TrunkingV1OriginationUrl
            - name: TrunkingV1PhoneNumber
            - name: TrunkingV1Recording
            - name: TrunkingV1Trunk
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/trunking-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/trunking-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---