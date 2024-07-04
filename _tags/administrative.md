---
name: Administrative
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/administrative.png
url: https://example.com/apis/administrative.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Administrative
apis:
  - name: Adyen Terminal API
    description: >-
      The Adyen Terminal API lets you make payments, issue refunds, collect
      shopper information, and perform other shopper-terminal interactions using
      a payment terminal supplied by Adyen.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/point-of-sale/design-your-integration/terminal-api/terminal-api-reference/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/point-of-sale/design-your-integration/terminal-api/terminal-api-reference/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Adyen Terminal API
          paths:
            /login:
              post:
                description: >-
                  It conveys Information related to the session (period between
                  a Login and the following Logout) to process. Content of the
                  Login Request message.
                summary: Login Request
                tags:
                  - Login
                  - Request
                  - Login
            /logout:
              post:
                description: Empty. Content of the Logout Request message.
                summary: Logout Request
                tags:
                  - Logout
                  - Request
                  - Login
                  - Logout
            /enableservice:
              post:
                description: >-
                  It conveys the services that will be enabled for the  POI
                  Terminal without the request of the Sale System, and a
                  possible invitation for the Customer to start the services.
                  Content of the Enable Service Request message.
                summary: EnableService Request
                tags:
                  - Enable
                  - Services
                  - Request
                  - Login
                  - Logout
                  - Enable Service
            /admin:
              post:
                description: Empty. Content of the Custom Admin Request message.
                summary: Admin Request
                tags:
                  - Administrative
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
            /payment:
              post:
                description: >-
                  Request sent to terminal to initiate payment.  It conveys
                  Information related to the Payment transaction to process.
                  Content of the Payment Request message.
                summary: Payment Request
                tags:
                  - Payments
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
            /cardacquisition:
              post:
                description: >-
                  It conveys Information related to the payment and loyalty
                  cards to read and analyse. This message pair is usually
                  followed by a message pair (e.g. payment or loyalty) which
                  refers to this Card Acquisition message pair. Content of the
                  Card Acquisition Request message.
                summary: CardAcquisition Request
                tags:
                  - Cards
                  - Acquisition
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
            /loyalty:
              post:
                description: >-
                  It conveys Information related to the Loyalty transaction to
                  process. Content of the Loyalty Request message.
                summary: Loyalty Request
                tags:
                  - Loyalty
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
            /storedvalue:
              post:
                description: >-
                  It conveys Information related to the Stored Value transaction
                  to process. Content of the Stored Value Request message.
                summary: StoredValue Request
                tags:
                  - Stored
                  - Value
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
            /reversal:
              post:
                description: >-
                  It conveys Information related to the reversal of a previous
                  payment or a loyalty transaction. Content of the Reversal
                  Request message.
                summary: Reversal Request
                tags:
                  - Reversals
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
            /reconciliation:
              post:
                description: >-
                  It conveys Information related to the Reconciliation requested
                  by the Sale System. Content of the Reconciliation Request
                  message.
                summary: Reconciliation Request
                tags:
                  - Reconciliation
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
            /gettotals:
              post:
                description: >-
                  It conveys information from the Sale System related to the
                  scope and the format of the totals to be computed by the POI
                  System. Content of the Get Totals Request message.
                summary: GetTotals Request
                tags:
                  - Get
                  - Totals
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
            /balanceinquiry:
              post:
                description: >-
                  It conveys Information related to the account for which a
                  Balance Inquiry is requested. Content of the Balance Inquiry
                  Request message.
                summary: BalanceInquiry Request
                tags:
                  - Balance
                  - Inquiries
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
            /transactionstatus:
              post:
                description: >-
                  It conveys Information requested for status of the last or
                  current Payment, Loyalty or Reversal transaction. Content of
                  the TransactionStatus Request message.
                summary: TransactionStatus Request
                tags:
                  - Transactions
                  - Status
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
            /diagnosis:
              post:
                description: >-
                  It conveys Information related to the target POI for which the
                  diagnosis is requested. Content of the Diagnosis Request
                  message.
                summary: Diagnosis Request
                tags:
                  - Diagnosis
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
            /display:
              post:
                description: >-
                  It conveys the data to display and the way to process the
                  display. It contains the complete content to display. It might
                  contain an operation (the DisplayOutput element) per Display
                  Device type. Content of the Display Request message.
                summary: Display Request
                tags:
                  - Display
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
            /input:
              post:
                description: >-
                  It conveys data to display and the way to process the display,
                  and contains the complete content to display. In addition to
                  the display on the Input Device, it might contain an operation
                  (the DisplayOutput element) per Display Device type. Content
                  of the Input Request message.
                summary: Input Request
                tags:
                  - Inputs
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
            /print:
              post:
                description: >-
                  It conveys the data to print and the way to process the print.
                  It contains the complete content to print. Content of the
                  Print Request message.
                summary: Print Request
                tags:
                  - Print
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
                  - Print
            /cardreaderapdu:
              post:
                description: >-
                  It contains the APDU request to send to the chip of the card,
                  and a possible invitation message to display on the
                  CashierInterface or the CustomerInterface. Content of the Card
                  Reader APDU Request message.
                summary: CardReaderAPDU Reque
                tags:
                  - Cards
                  - Readers
                  - Reque
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
                  - Print
                  - Card Reader Applications
    overlays:
      - type: APIs.io Search
        url: overlays/terminal-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/terminal-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-terminal-api
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
  - name: chime
    description: >-
      <important> <p> <b>Most of these APIs are no longer supported and will not
      be updated.</b> We recommend using the latest versions in the <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/welcome.html">Amazon
      Chime SDK API reference</a>, in the Amazon Chime SDK.</p> <p>Using the
      latest versions requires migrating to dedicated namespaces. For more
      information, refer to <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
      from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK Developer
      Guide</i>.</p> </important> <p>The Amazon Chime application programming
      interface (API) is designed so administrators can perform key tasks, such
      as creating and managing Amazon Chime accounts, users, and Voice
      Connectors. This guide provides detailed information about the Amazon
      Chime API, including operations, types, inputs and outputs, and error
      codes.</p> <p>You can use an AWS SDK, the AWS Command Line Interface (AWS
      CLI), or the REST API to make API calls for Amazon Chime. We recommend
      using an AWS SDK or the AWS CLI. The page for each API action contains a
      <i>See Also</i> section that includes links to information about using the
      action with a language-specific AWS SDK or the AWS CLI.</p> <dl> <dt>Using
      an AWS SDK</dt> <dd> <p> You don't need to write code to calculate a
      signature for request authentication. The SDK clients authenticate your
      requests by using access keys that you provide. For more information about
      AWS SDKs, see the <a href="http://aws.amazon.com/developer/">AWS Developer
      Center</a>. </p> </dd> <dt>Using the AWS CLI</dt> <dd> <p>Use your access
      keys with the AWS CLI to make API calls. For information about setting up
      the AWS CLI, see <a
      href="https://docs.aws.amazon.com/cli/latest/userguide/installing.html">Installing
      the AWS Command Line Interface</a> in the <i>AWS Command Line Interface
      User Guide</i>. For a list of available Amazon Chime commands, see the <a
      href="https://docs.aws.amazon.com/cli/latest/reference/chime/index.html">Amazon
      Chime commands</a> in the <i>AWS CLI Command Reference</i>. </p> </dd>
      <dt>Using REST APIs</dt> <dd> <p>If you use REST to make API calls, you
      must authenticate your request by providing a signature. Amazon Chime
      supports Signature Version 4. For more information, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
      Version 4 Signing Process</a> in the <i>Amazon Web Services General
      Reference</i>.</p> <p>When making REST API calls, use the service name
      <code>chime</code> and REST endpoint
      <code>https://service.chime.aws.amazon.com</code>.</p> </dd> </dl>
      <p>Administrative permissions are controlled using AWS Identity and Access
      Management (IAM). For more information, see <a
      href="https://docs.aws.amazon.com/chime/latest/ag/security-iam.html">Identity
      and Access Management for Amazon Chime</a> in the <i>Amazon Chime
      Administration Guide</i>.</p>
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
            title: chime
          paths:
            /accounts/{accountId}/users/{userId}?operation=associate-phone-number:
              POST:
                summary: AssociatePhoneNumberWithUser
                description: >-
                  <p>Associates a phone number with the specified Amazon Chime
                  user.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
            /voice-connectors/{voiceConnectorId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnector
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_AssociatePhoneNumbersWithVoiceConnector.html">AssociatePhoneNumbersWithVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
            /voice-connector-groups/{voiceConnectorGroupId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnectorGroup
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  Voice Connector group.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_AssociatePhoneNumbersWithVoiceConnectorGroup.html">AssociatePhoneNumbersWithVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Voice
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
            /accounts/{accountId}?operation=associate-signin-delegate-groups:
              POST:
                summary: AssociateSigninDelegateGroupsWithAccount
                description: >-
                  <p>Associates the specified sign-in delegate groups with the
                  specified Amazon Chime account.</p>
                tags:
                  - Associate
                  - Sign In
                  - Delegate
                  - Groups
                  - With
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
            /meetings/{meetingId}/attendees?operation=batch-create:
              POST:
                summary: BatchCreateAttendee
                description: >-
                  <p>Creates up to 100 new attendees for an active Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_BatchCreateAttendee.html">BatchCreateAttendee</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p>For more information
                  about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p>
                tags:
                  - Batches
                  - Create
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
            /channels/{channelArn}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateChannelMembership
                description: >-
                  <p>Adds a specified number of users to a channel.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_BatchCreateChannelMembership.html">BatchCreateChannelMembership</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Batches
                  - Create
                  - Channels
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
            /accounts/{accountId}/rooms/{roomId}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateRoomMembership
                description: >-
                  <p>Adds up to 50 members to a chat room in an Amazon Chime
                  Enterprise account. Members can be users or bots. The member
                  role designates whether the member is a chat room
                  administrator or a general chat room member.</p>
                tags:
                  - Batches
                  - Create
                  - Rooms
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
            /phone-numbers?operation=batch-delete:
              POST:
                summary: BatchDeletePhoneNumber
                description: >-
                  <p> Moves phone numbers into the <b>Deletion queue</b>. Phone
                  numbers must be disassociated from any users or Amazon Chime
                  Voice Connectors before they can be deleted. </p> <p> Phone
                  numbers remain in the <b>Deletion queue</b> for 7 days before
                  they are deleted permanently. </p>
                tags:
                  - Batches
                  - Delete
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
            /accounts/{accountId}/users?operation=suspend:
              POST:
                summary: BatchSuspendUser
                description: >-
                  <p>Suspends up to 50 users from a <code>Team</code> or
                  <code>EnterpriseLWA</code> Amazon Chime account. For more
                  information about different account types, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/manage-chime-account.html">Managing
                  Your Amazon Chime Accounts</a> in the <i>Amazon Chime
                  Administration Guide</i>.</p> <p>Users suspended from a
                  <code>Team</code> account are disassociated from the
                  account,but they can continue to use Amazon Chime as free
                  users. To remove the suspension from suspended
                  <code>Team</code> account users, invite them to the
                  <code>Team</code> account again. You can use the
                  <a>InviteUsers</a> action to do so.</p> <p>Users suspended
                  from an <code>EnterpriseLWA</code> account are immediately
                  signed out of Amazon Chime and can no longer sign in. To
                  remove the suspension from suspended
                  <code>EnterpriseLWA</code> account users, use the
                  <a>BatchUnsuspendUser</a> action.</p> <p> To sign out users
                  without suspending them, use the <a>LogoutUser</a> action.</p>
                tags:
                  - Batches
                  - Suspend
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
            /accounts/{accountId}/users?operation=unsuspend:
              POST:
                summary: BatchUnsuspendUser
                description: >-
                  <p>Removes the suspension from up to 50 previously suspended
                  users for the specified Amazon Chime
                  <code>EnterpriseLWA</code> account. Only users on
                  <code>EnterpriseLWA</code> accounts can be unsuspended using
                  this action. For more information about different account
                  types, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/manage-chime-account.html">
                  Managing Your Amazon Chime Accounts </a> in the account types,
                  in the <i>Amazon Chime Administration Guide</i>. </p>
                  <p>Previously suspended users who are unsuspended using this
                  action are returned to <code>Registered</code> status. Users
                  who are not previously suspended are ignored.</p>
                tags:
                  - Batches
                  - Unsuspend
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
            /phone-numbers?operation=batch-update:
              POST:
                summary: BatchUpdatePhoneNumber
                description: >-
                  <p>Updates phone number product types or calling names. You
                  can update one attribute at a time for each
                  <code>UpdatePhoneNumberRequestItem</code>. For example, you
                  can update the product type or the calling name.</p> <p>For
                  toll-free numbers, you cannot use the Amazon Chime Business
                  Calling product type. For numbers outside the U.S., you must
                  use the Amazon Chime SIP Media Application Dial-In product
                  type.</p> <p>Updates to outbound calling names can take up to
                  72 hours to complete. Pending updates to outbound calling
                  names must be complete before you can request another
                  update.</p>
                tags:
                  - Batches
                  - Update
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
            /accounts/{accountId}/users:
              GET:
                summary: ListUsers
                description: >-
                  <p>Lists the users that belong to the specified Amazon Chime
                  account. You can specify an email address to list only the
                  user that the email address belongs to.</p>
                tags:
                  - Lists
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
            /accounts:
              GET:
                summary: ListAccounts
                description: >-
                  <p>Lists the Amazon Chime accounts under the administrator's
                  AWS account. You can filter accounts by account name prefix.
                  To find out which Amazon Chime account a user belongs to, you
                  can filter by the user's email address, which returns one
                  account result.</p>
                tags:
                  - Lists
                  - Accounts
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
            /app-instances:
              GET:
                summary: ListAppInstances
                description: >-
                  <p>Lists all Amazon Chime <code>AppInstance</code>s created
                  under a single AWS account.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstances.html">ListAppInstances</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
            /app-instances/{appInstanceArn}/admins:
              GET:
                summary: ListAppInstanceAdmins
                description: >-
                  <p>Returns a list of the administrators in the
                  <code>AppInstance</code>.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstanceAdmins.html">ListAppInstanceAdmins</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Administrator
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
            /app-instance-users:
              GET:
                summary: ListAppInstanceUsers
                description: >-
                  <p>List all <code>AppInstanceUsers</code> created under a
                  single <code>AppInstance</code>. </p> <important> <p> <b>This
                  API is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstanceUsers.html">ListAppInstanceUsers</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
            /meetings/{meetingId}/attendees:
              GET:
                summary: ListAttendees
                description: >-
                  <p> Lists the attendees for the specified Amazon Chime SDK
                  meeting. For more information about the Amazon Chime SDK, see
                  <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListAttendees.html">ListAttendees</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
            /accounts/{accountId}/bots:
              GET:
                summary: ListBots
                description: >-
                  <p>Lists the bots associated with the administrator's Amazon
                  Chime Enterprise account ID.</p>
                tags:
                  - Lists
                  - Bots
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
            /channels:
              GET:
                summary: ListChannels
                description: >-
                  <p>Lists all Channels created under a single Chime App as a
                  paginated list. You can specify filters to narrow results.</p>
                  <p class="title"> <b>Functionality &amp; restrictions</b> </p>
                  <ul> <li> <p>Use privacy = <code>PUBLIC</code> to retrieve all
                  public channels in the account.</p> </li> <li> <p>Only an
                  <code>AppInstanceAdmin</code> can set privacy =
                  <code>PRIVATE</code> to list the private channels in an
                  account.</p> </li> </ul> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannels.html">ListChannels</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
            /channels/{channelArn}/bans:
              GET:
                summary: ListChannelBans
                description: >-
                  <p>Lists all the users banned from a particular channel.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelBans.html">ListChannelBans</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Bans
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
            /channels/{channelArn}/memberships:
              GET:
                summary: ListChannelMemberships
                description: >-
                  <p>Lists all channel memberships in a channel.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelMemberships.html">ListChannelMemberships</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
            /channels/{channelArn}/moderators:
              GET:
                summary: ListChannelModerators
                description: >-
                  <p>Lists all the moderators for a channel.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelModerators.html">ListChannelModerators</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Moderators
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
            /media-capture-pipelines:
              GET:
                summary: ListMediaCapturePipelines
                description: >-
                  <p>Returns a list of media capture pipelines.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_media-pipelines-chime_ListMediaCapturePipelines.html">ListMediaCapturePipelines</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Media
                  - Capture
                  - Pipelines
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
            /meetings:
              GET:
                summary: ListMeetings
                description: >-
                  <p>Lists up to 100 active Amazon Chime SDK meetings.</p>
                  <important> <p>ListMeetings is not supported in the Amazon
                  Chime SDK Meetings Namespace. Update your application to
                  remove calls to this API.</p> </important> <p>For more
                  information about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
            /meetings/{meetingId}/dial-outs:
              POST:
                summary: CreateMeetingDialOut
                description: >-
                  <p>Uses the join token and call metadata in a meeting request
                  (From number, To number, and so forth) to initiate an outbound
                  call to a public switched telephone network (PSTN) and join
                  them into a Chime meeting. Also ensures that the From number
                  belongs to the customer.</p> <p>To play welcome audio or
                  implement an interactive voice response (IVR), use the
                  <code>CreateSipMediaApplicationCall</code> action with the
                  corresponding SIP media application ID.</p> <important> <p>
                  <b>This API is is not available in a dedicated namespace.</b>
                  </p> </important>
                tags:
                  - Create
                  - Meetings
                  - Dial
                  - Out
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
            /meetings?operation=create-attendees:
              POST:
                summary: CreateMeetingWithAttendees
                description: >-
                  <p> Creates a new Amazon Chime SDK meeting in the specified
                  media Region, with attendees. For more information about
                  specifying media Regions, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/chime-sdk-meetings-regions.html">Amazon
                  Chime SDK Media Regions</a> in the <i>Amazon Chime SDK
                  Developer Guide</i> . For more information about the Amazon
                  Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i> . </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_CreateMeetingWithAttendees.html">CreateMeetingWithAttendees</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Create
                  - Meetings
                  - With
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
            /phone-number-orders:
              GET:
                summary: ListPhoneNumberOrders
                description: >-
                  <p>Lists the phone number orders for the administrator's
                  Amazon Chime account.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Orders
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
            /voice-connectors/{voiceConnectorId}/proxy-sessions:
              GET:
                summary: ListProxySessions
                description: >-
                  <p>Lists the proxy sessions for the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListProxySessions.html">ListProxySessions</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Proxy
                  - Sessions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /accounts/{accountId}/rooms:
              GET:
                summary: ListRooms
                description: >-
                  <p>Lists the room details for the specified Amazon Chime
                  Enterprise account. Optionally, filter the results by a member
                  ID (user ID or bot ID) to see a list of rooms that the member
                  belongs to.</p>
                tags:
                  - Lists
                  - Rooms
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}/memberships:
              GET:
                summary: ListRoomMemberships
                description: >-
                  <p>Lists the membership details for the specified room in an
                  Amazon Chime Enterprise account, such as the members' IDs,
                  email addresses, and names.</p>
                tags:
                  - Lists
                  - Rooms
                  - Memberships
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /sip-media-applications:
              GET:
                summary: ListSipMediaApplications
                description: >-
                  <p>Lists the SIP media applications under the administrator's
                  AWS account.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListSipMediaApplications.html">ListSipMediaApplications</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - SIP
                  - Media
                  - Applications
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
            /sip-media-applications/{sipMediaApplicationId}/calls:
              POST:
                summary: CreateSipMediaApplicationCall
                description: >-
                  <p>Creates an outbound call to a phone number from the phone
                  number specified in the request, and it invokes the endpoint
                  of the specified <code>sipMediaApplicationId</code>.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_CreateSipMediaApplicationCall.html">CreateSipMediaApplicationCall</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Create
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
            /sip-rules:
              GET:
                summary: ListSipRules
                description: >-
                  <p>Lists the SIP rules under the administrator's AWS
                  account.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListSipRules.html">ListSipRules</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - SIP
                  - Rules
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
            /accounts/{accountId}/users?operation=create:
              POST:
                summary: CreateUser
                description: >-
                  <p>Creates a user under the specified Amazon Chime
                  account.</p>
                tags:
                  - Create
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
            /voice-connectors:
              GET:
                summary: ListVoiceConnectors
                description: >-
                  <p>Lists the Amazon Chime Voice Connectors for the
                  administrator's AWS account.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectors.html">ListVoiceConnectors</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /voice-connector-groups:
              GET:
                summary: ListVoiceConnectorGroups
                description: >-
                  <p>Lists the Amazon Chime Voice Connector groups for the
                  administrator's AWS account.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectorGroups.html">ListVoiceConnectorGroups</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Groups
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /accounts/{accountId}:
              POST:
                summary: UpdateAccount
                description: >-
                  <p>Updates account details for the specified Amazon Chime
                  account. Currently, only account name and default license
                  updates are supported for this action.</p>
                tags:
                  - Update
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /app-instances/{appInstanceArn}:
              PUT:
                summary: UpdateAppInstance
                description: >-
                  <p>Updates <code>AppInstance</code> metadata.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_UpdateAppInstance.html">UpdateAppInstance</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /app-instances/{appInstanceArn}/admins/{appInstanceAdminArn}:
              GET:
                summary: DescribeAppInstanceAdmin
                description: >-
                  <p>Returns the full details of an
                  <code>AppInstanceAdmin</code>.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_DescribeAppInstanceAdmin.html">DescribeAppInstanceAdmin</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Applications
                  - Instances
                  - Administrative
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
            /app-instances/{appInstanceArn}/streaming-configurations:
              PUT:
                summary: PutAppInstanceStreamingConfigurations
                description: >-
                  <p>The data streaming configurations of an
                  <code>AppInstance</code>.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_PutMessagingStreamingConfigurations.html">PutMessagingStreamingConfigurations</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Streaming
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
            /app-instance-users/{appInstanceUserArn}:
              PUT:
                summary: UpdateAppInstanceUser
                description: >-
                  <p>Updates the details of an <code>AppInstanceUser</code>. You
                  can update names and metadata.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_UpdateAppInstanceUser.html">UpdateAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
            /meetings/{meetingId}/attendees/{attendeeId}:
              GET:
                summary: GetAttendee
                description: >-
                  <p> Gets the Amazon Chime SDK attendee details for a specified
                  meeting ID and attendee ID. For more information about the
                  Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_GetAttendee.html">GetAttendee</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
            /channels/{channelArn}:
              PUT:
                summary: UpdateChannel
                description: >-
                  <p>Update a channel's attributes.</p> <p> <b>Restriction</b>:
                  You can't change a channel's privacy. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannel.html">UpdateChannel</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
            /channels/{channelArn}/bans/{memberArn}:
              GET:
                summary: DescribeChannelBan
                description: >-
                  <p>Returns the full details of a channel ban.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelBan.html">DescribeChannelBan</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Ban
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
            /channels/{channelArn}/memberships/{memberArn}:
              GET:
                summary: DescribeChannelMembership
                description: >-
                  <p>Returns the full details of a user's channel
                  membership.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelMembership.html">DescribeChannelMembership</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
            /channels/{channelArn}/messages/{messageId}:
              PUT:
                summary: UpdateChannelMessage
                description: >-
                  <p>Updates the content of a message.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannelMessage.html">UpdateChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
            /channels/{channelArn}/moderators/{channelModeratorArn}:
              GET:
                summary: DescribeChannelModerator
                description: >-
                  <p>Returns the full details of a single ChannelModerator.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelModerator.html">DescribeChannelModerator</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Moderators
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
            /accounts/{accountId}/bots/{botId}/events-configuration:
              PUT:
                summary: PutEventsConfiguration
                description: >-
                  <p>Creates an events configuration that allows a bot to
                  receive outgoing events sent by Amazon Chime. Choose either an
                  HTTPS endpoint or a Lambda function ARN. For more information,
                  see <a>Bot</a>.</p>
                tags:
                  - Put
                  - Events
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
            /media-capture-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaCapturePipeline
                description: >-
                  <p>Gets an existing media capture pipeline.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_media-pipelines-chime_GetMediaCapturePipeline.html">GetMediaCapturePipeline</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Media
                  - Capture
                  - Pipelines
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /meetings/{meetingId}:
              GET:
                summary: GetMeeting
                description: >-
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_GetMeeting.html">GetMeeting</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p> Gets the Amazon
                  Chime SDK meeting details for the specified meeting ID. For
                  more information about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i> . </p>
                tags:
                  - Get
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /phone-numbers/{phoneNumberId}:
              POST:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates phone number details, such as product type or
                  calling name, for the specified phone number ID. You can
                  update one phone number detail at a time. For example, you can
                  update either the product type or the calling name in one
                  action.</p> <p>For toll-free numbers, you cannot use the
                  Amazon Chime Business Calling product type. For numbers
                  outside the U.S., you must use the Amazon Chime SIP Media
                  Application Dial-In product type.</p> <p>Updates to outbound
                  calling names can take 72 hours to complete. Pending updates
                  to outbound calling names must be complete before you can
                  request another update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /voice-connectors/{voiceConnectorId}/proxy-sessions/{proxySessionId}:
              POST:
                summary: UpdateProxySession
                description: >-
                  <p>Updates the specified proxy session details, such as voice
                  or SMS capabilities.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateProxySession.html">UpdateProxySession</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Proxy
                  - Sessions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}:
              POST:
                summary: UpdateRoom
                description: >-
                  <p>Updates room details, such as the room name, for a room in
                  an Amazon Chime Enterprise account.</p>
                tags:
                  - Update
                  - Rooms
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}/memberships/{memberId}:
              POST:
                summary: UpdateRoomMembership
                description: >-
                  <p>Updates room membership details, such as the member role,
                  for a room in an Amazon Chime Enterprise account. The member
                  role designates whether the member is a chat room
                  administrator or a general chat room member. The member role
                  can be updated only for user IDs.</p>
                tags:
                  - Update
                  - Rooms
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /sip-media-applications/{sipMediaApplicationId}:
              PUT:
                summary: UpdateSipMediaApplication
                description: >-
                  <p>Updates the details of the specified SIP media
                  application.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipMediaApplication.html">UpdateSipMediaApplication</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /sip-rules/{sipRuleId}:
              PUT:
                summary: UpdateSipRule
                description: >-
                  <p>Updates the details of the specified SIP rule.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipRule.html">UpdateSipRule</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Rules
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}:
              PUT:
                summary: UpdateVoiceConnector
                description: >-
                  <p>Updates details for the specified Amazon Chime Voice
                  Connector.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateVoiceConnector.html">UpdateVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}/emergency-calling-configuration:
              PUT:
                summary: PutVoiceConnectorEmergencyCallingConfiguration
                description: >-
                  <p>Puts emergency calling configuration details to the
                  specified Amazon Chime Voice Connector, such as emergency
                  phone numbers and calling countries. Origination and
                  termination settings must be enabled for the Amazon Chime
                  Voice Connector before emergency calling can be
                  configured.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorEmergencyCallingConfiguration.html">PutVoiceConnectorEmergencyCallingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Emergency
                  - Calling
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
            /voice-connector-groups/{voiceConnectorGroupId}:
              PUT:
                summary: UpdateVoiceConnectorGroup
                description: >-
                  <p>Updates details of the specified Amazon Chime Voice
                  Connector group, such as the name and Amazon Chime Voice
                  Connector priority ranking.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateVoiceConnectorGroup.html">UpdateVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Voice
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
            /voice-connectors/{voiceConnectorId}/origination:
              PUT:
                summary: PutVoiceConnectorOrigination
                description: >-
                  <p>Adds origination settings for the specified Amazon Chime
                  Voice Connector.</p> <note> <p>If emergency calling is
                  configured for the Amazon Chime Voice Connector, it must be
                  deleted prior to turning off origination settings.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorOrigination.html">PutVoiceConnectorOrigination</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Origination
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
            /voice-connectors/{voiceConnectorId}/programmable-numbers/proxy:
              PUT:
                summary: PutVoiceConnectorProxy
                description: >-
                  <p>Puts the specified proxy configuration to the specified
                  Amazon Chime Voice Connector.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorProxy.html">PutVoiceConnectorProxy</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Proxy
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/streaming-configuration:
              PUT:
                summary: PutVoiceConnectorStreamingConfiguration
                description: >-
                  <p>Adds a streaming configuration for the specified Amazon
                  Chime Voice Connector. The streaming configuration specifies
                  whether media streaming is enabled for sending to Kinesis. It
                  also sets the retention period, in hours, for the Amazon
                  Kinesis data.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorStreamingConfiguration.html">PutVoiceConnectorStreamingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Streaming
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/termination:
              PUT:
                summary: PutVoiceConnectorTermination
                description: >-
                  <p>Adds termination settings for the specified Amazon Chime
                  Voice Connector.</p> <note> <p>If emergency calling is
                  configured for the Amazon Chime Voice Connector, it must be
                  deleted prior to turning off termination settings.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorTermination.html">PutVoiceConnectorTermination</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Termination
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=delete:
              POST:
                summary: DeleteVoiceConnectorTerminationCredentials
                description: >-
                  <p>Deletes the specified SIP credentials used by your
                  equipment to authenticate during call termination.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DeleteVoiceConnectorTerminationCredentials.html">DeleteVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Delete
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
            /channels/{channelArn}?scope=app-instance-user-membership:
              GET:
                summary: DescribeChannelMembershipForAppInstanceUser
                description: >-
                  <p> Returns the details of a channel based on the membership
                  of the specified <code>AppInstanceUser</code>.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelMembershipForAppInstanceUser.html">DescribeChannelMembershipForAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - For
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
            /channels/{channelArn}?scope=app-instance-user-moderated-channel:
              GET:
                summary: DescribeChannelModeratedByAppInstanceUser
                description: >-
                  <p>Returns the full details of a channel moderated by the
                  specified <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelModeratedByAppInstanceUser.html">DescribeChannelModeratedByAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
            /accounts/{accountId}/users/{userId}?operation=disassociate-phone-number:
              POST:
                summary: DisassociatePhoneNumberFromUser
                description: >-
                  <p>Disassociates the primary provisioned phone number from the
                  specified Amazon Chime user.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /voice-connectors/{voiceConnectorId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnector
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime Voice Connector.</p> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DisassociatePhoneNumbersFromVoiceConnector.html">DisassociatePhoneNumbersFromVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /voice-connector-groups/{voiceConnectorGroupId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnectorGroup
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime Voice Connector group.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DisassociatePhoneNumbersFromVoiceConnectorGroup.html">DisassociatePhoneNumbersFromVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Voice
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /accounts/{accountId}?operation=disassociate-signin-delegate-groups:
              POST:
                summary: DisassociateSigninDelegateGroupsFromAccount
                description: >-
                  <p>Disassociates the specified sign-in delegate groups from
                  the specified Amazon Chime account.</p>
                tags:
                  - Disassociate
                  - Sign In
                  - Delegate
                  - Groups
                  - From
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /accounts/{accountId}/settings:
              PUT:
                summary: UpdateAccountSettings
                description: >-
                  <p>Updates the settings for the specified Amazon Chime
                  account. You can update settings for remote control of shared
                  screens, or for the dial-out option. For more information
                  about these settings, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/policies.html">Use
                  the Policies Page</a> in the <i>Amazon Chime Administration
                  Guide</i>.</p>
                tags:
                  - Update
                  - Account
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
            /app-instances/{appInstanceArn}/retention-settings:
              PUT:
                summary: PutAppInstanceRetentionSettings
                description: >-
                  <p>Sets the amount of time in days that a given
                  <code>AppInstance</code> retains data.</p> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_PutAppInstanceRetentionSettings.html">PutAppInstanceRetentionSettings</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Retention
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /accounts/{accountId}/bots/{botId}:
              POST:
                summary: UpdateBot
                description: >-
                  <p>Updates the status of the specified bot, such as starting
                  or stopping the bot from running in your Amazon Chime
                  Enterprise account.</p>
                tags:
                  - Update
                  - Bot
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates global settings for the administrator's AWS
                  account, such as Amazon Chime Business Calling and Amazon
                  Chime Voice Connector settings.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /endpoints/messaging-session:
              GET:
                summary: GetMessagingSessionEndpoint
                description: >-
                  <p>The details of the endpoint for the messaging session.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_GetMessagingSessionEndpoint.html">GetMessagingSessionEndpoint</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Messaging
                  - Sessions
                  - Endpoints
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
            /phone-number-orders/{phoneNumberOrderId}:
              GET:
                summary: GetPhoneNumberOrder
                description: >-
                  <p>Retrieves details for the specified phone number order,
                  such as the order creation timestamp, phone numbers in E.164
                  format, product type, and order status.</p>
                tags:
                  - Get
                  - Phone
                  - Numbers
                  - Orders
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /settings/phone-number:
              PUT:
                summary: UpdatePhoneNumberSettings
                description: >-
                  <p>Updates the phone number settings for the administrator's
                  AWS account, such as the default outbound calling name. You
                  can update the default outbound calling name once every seven
                  days. Outbound calling names can take up to 72 hours to
                  update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /accounts/{accountId}/retention-settings:
              PUT:
                summary: PutRetentionSettings
                description: >-
                  <p> Puts retention settings for the specified Amazon Chime
                  Enterprise account. We recommend using AWS CloudTrail to
                  monitor usage of this API for your account. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/cloudtrail.html">Logging
                  Amazon Chime API Calls with AWS CloudTrail</a> in the
                  <i>Amazon Chime Administration Guide</i>.</p> <p> To turn off
                  existing retention settings, remove the number of days from
                  the corresponding <b>RetentionDays</b> field in the
                  <b>RetentionSettings</b> object. For more information about
                  retention settings, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/chat-retention.html">Managing
                  Chat Retention Policies</a> in the <i>Amazon Chime
                  Administration Guide</i>.</p>
                tags:
                  - Put
                  - Retention
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /sip-media-applications/{sipMediaApplicationId}/logging-configuration:
              PUT:
                summary: PutSipMediaApplicationLoggingConfiguration
                description: >-
                  <p>Updates the logging configuration for the specified SIP
                  media application.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutSipMediaApplicationLoggingConfiguration.html">PutSipMediaApplicationLoggingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Logging
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /accounts/{accountId}/users/{userId}:
              POST:
                summary: UpdateUser
                description: >-
                  <p>Updates user details for a specified user ID. Currently,
                  only <code>LicenseType</code> updates are supported for this
                  action.</p>
                tags:
                  - Update
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /accounts/{accountId}/users/{userId}/settings:
              PUT:
                summary: UpdateUserSettings
                description: >-
                  <p>Updates the settings for the specified user, such as phone
                  number settings.</p>
                tags:
                  - Update
                  - Users
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /voice-connectors/{voiceConnectorId}/logging-configuration:
              PUT:
                summary: PutVoiceConnectorLoggingConfiguration
                description: >-
                  <p>Adds a logging configuration for the specified Amazon Chime
                  Voice Connector. The logging configuration specifies whether
                  SIP message logs are enabled for sending to Amazon CloudWatch
                  Logs.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorLoggingConfiguration.html">PutVoiceConnectorLoggingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Logging
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /voice-connectors/{voiceConnectorId}/termination/health:
              GET:
                summary: GetVoiceConnectorTerminationHealth
                description: >-
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_GetVoiceConnectorTerminationHealth.html">GetVoiceConnectorTerminationHealth</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p>Retrieves information
                  about the last time a SIP <code>OPTIONS</code> ping was
                  received from your SIP infrastructure for the specified Amazon
                  Chime Voice Connector.</p>
                tags:
                  - Get
                  - Voice
                  - Connectors
                  - Termination
                  - Health
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
            /accounts/{accountId}/users?operation=add:
              POST:
                summary: InviteUsers
                description: >-
                  <p>Sends email to a maximum of 50 users, inviting them to the
                  specified Amazon Chime <code>Team</code> account. Only
                  <code>Team</code> account types are currently supported for
                  this action.</p>
                tags:
                  - Invite
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
            /meetings/{meetingId}/attendees/{attendeeId}/tags:
              GET:
                summary: ListAttendeeTags
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK attendee
                  resource.</p> <important> <p>ListAttendeeTags is not supported
                  in the Amazon Chime SDK Meetings Namespace. Update your
                  application to remove calls to this API.</p> </important>
                tags:
                  - Lists
                  - Attendees
                  - Tags
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
            /channels?scope=app-instance-user-memberships:
              GET:
                summary: ListChannelMembershipsForAppInstanceUser
                description: >-
                  <p> Lists all channels that a particular
                  <code>AppInstanceUser</code> is a part of. Only an
                  <code>AppInstanceAdmin</code> can call the API with a user ARN
                  that is not their own. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelMembershipsForAppInstanceUser.html">ListChannelMembershipsForAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - For
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /channels/{channelArn}/messages:
              POST:
                summary: SendChannelMessage
                description: >-
                  <p>Sends a message to a particular channel that the member is
                  a part of.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> <p>Also,
                  <code>STANDARD</code> messages can contain 4KB of data and the
                  1KB of metadata. <code>CONTROL</code> messages can contain 30
                  bytes of data and no metadata.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_SendChannelMessage.html">SendChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Send
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /channels?scope=app-instance-user-moderated-channels:
              GET:
                summary: ListChannelsModeratedByAppInstanceUser
                description: >-
                  <p>A list of the channels moderated by an
                  <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelsModeratedByAppInstanceUser.html">ListChannelsModeratedByAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /meetings/{meetingId}/tags:
              GET:
                summary: ListMeetingTags
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK meeting
                  resource.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListTagsForResource.html">ListTagsForResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Meetings
                  - Tags
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /phone-numbers:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Lists the phone numbers for the specified Amazon Chime
                  account, Amazon Chime user, Amazon Chime Voice Connector, or
                  Amazon Chime Voice Connector group.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /phone-number-countries:
              GET:
                summary: ListSupportedPhoneNumberCountries
                description: <p>Lists supported phone number countries.</p>
                tags:
                  - Lists
                  - Supported
                  - Phone
                  - Numbers
                  - Countries
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
            /tags:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK meeting and
                  messaging resources.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the applicable latest version in the Amazon Chime
                  SDK.</p> <ul> <li> <p>For meetings: <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListTagsForResource.html">ListTagsForResource</a>.</p>
                  </li> <li> <p>For messaging: <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListTagsForResource.html">ListTagsForResource</a>.</p>
                  </li> </ul> <p>Using the latest version requires migrating to
                  a dedicated namespace. For more information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
            /voice-connectors/{voiceConnectorId}/termination/credentials:
              GET:
                summary: ListVoiceConnectorTerminationCredentials
                description: >-
                  <p>Lists the SIP credentials for the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectorTerminationCredentials.html">ListVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
            /accounts/{accountId}/users/{userId}?operation=logout:
              POST:
                summary: LogoutUser
                description: >-
                  <p>Logs out the specified user from all of the devices they
                  are currently logged into.</p>
                tags:
                  - Logout
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=put:
              POST:
                summary: PutVoiceConnectorTerminationCredentials
                description: >-
                  <p>Adds termination SIP credentials for the specified Amazon
                  Chime Voice Connector.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorTerminationCredentials.html">PutVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
            /channels/{channelArn}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactChannelMessage
                description: >-
                  <p>Redacts message content, but not metadata. The message
                  exists in the back end, but the action returns null content,
                  and the state shows as redacted.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_RedactChannelMessage.html">RedactChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Redact
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
            /accounts/{accountId}/conversations/{conversationId}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactConversationMessage
                description: >-
                  <p>Redacts the specified message from the specified Amazon
                  Chime conversation.</p>
                tags:
                  - Redact
                  - Conversations
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
            /accounts/{accountId}/rooms/{roomId}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactRoomMessage
                description: >-
                  <p>Redacts the specified message from the specified Amazon
                  Chime channel.</p>
                tags:
                  - Redact
                  - Rooms
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
            /accounts/{accountId}/bots/{botId}?operation=regenerate-security-token:
              POST:
                summary: RegenerateSecurityToken
                description: <p>Regenerates the security token for a bot.</p>
                tags:
                  - Regenerate
                  - Security
                  - Tokens
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
            /accounts/{accountId}/users/{userId}?operation=reset-personal-pin:
              POST:
                summary: ResetPersonalPIN
                description: >-
                  <p>Resets the personal meeting PIN for the specified user on
                  an Amazon Chime account. Returns the <a>User</a> object with
                  the updated personal meeting PIN.</p>
                tags:
                  - Reset
                  - Personal
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
            /phone-numbers/{phoneNumberId}?operation=restore:
              POST:
                summary: RestorePhoneNumber
                description: >-
                  <p>Moves a phone number from the <b>Deletion queue</b> back
                  into the phone number <b>Inventory</b>.</p>
                tags:
                  - Restore
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
            /search?type=phone-numbers:
              GET:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches for phone numbers that can be ordered. For US
                  numbers, provide at least one of the following search filters:
                  <code>AreaCode</code>, <code>City</code>, <code>State</code>,
                  or <code>TollFreePrefix</code>. If you provide
                  <code>City</code>, you must also provide <code>State</code>.
                  Numbers outside the US only support the
                  <code>PhoneNumberType</code> filter, which you must use.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
            /meetings/{meetingId}/transcription?operation=start:
              POST:
                summary: StartMeetingTranscription
                description: >-
                  <p>Starts transcription for the specified
                  <code>meetingId</code>. For more information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meeting-transcription.html">
                  Using Amazon Chime SDK live transcription </a> in the
                  <i>Amazon Chime SDK Developer Guide</i>.</p> <p>If you specify
                  an invalid configuration, a <code>TranscriptFailed</code>
                  event will be sent with the contents of the
                  <code>BadRequestException</code> generated by Amazon
                  Transcribe. For more information on each parameter and which
                  combinations are valid, refer to the <a
                  href="https://docs.aws.amazon.com/transcribe/latest/APIReference/API_streaming_StartStreamTranscription.html">StartStreamTranscription</a>
                  API in the <i>Amazon Transcribe Developer Guide</i>.</p>
                  <note> <p>Amazon Chime SDK live transcription is powered by
                  Amazon Transcribe. Use of Amazon Transcribe is subject to the
                  <a href="https://aws.amazon.com/service-terms/">AWS Service
                  Terms</a>, including the terms specific to the AWS Machine
                  Learning and Artificial Intelligence Services.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_StartMeetingTranscription.html">StartMeetingTranscription</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Start
                  - Meetings
                  - Transcriptions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
            /meetings/{meetingId}/transcription?operation=stop:
              POST:
                summary: StopMeetingTranscription
                description: >-
                  <p>Stops transcription for the specified
                  <code>meetingId</code>.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_StopMeetingTranscription.html">StopMeetingTranscription</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Stop
                  - Meetings
                  - Transcriptions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
            /meetings/{meetingId}/attendees/{attendeeId}/tags?operation=add:
              POST:
                summary: TagAttendee
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  attendee.</p> <important> <p>TagAttendee is not supported in
                  the Amazon Chime SDK Meetings Namespace. Update your
                  application to remove calls to this API.</p> </important>
                tags:
                  - Tags
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
            /meetings/{meetingId}/tags?operation=add:
              POST:
                summary: TagMeeting
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_TagResource.html">TagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Tags
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK meeting resource.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_TagResource.html">TagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Tags
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
            /meetings/{meetingId}/attendees/{attendeeId}/tags?operation=delete:
              POST:
                summary: UntagAttendee
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK attendee.</p> <important> <p>UntagAttendee is not
                  supported in the Amazon Chime SDK Meetings Namespace. Update
                  your application to remove calls to this API.</p> </important>
                tags:
                  - Untag
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
            /meetings/{meetingId}/tags?operation=delete:
              POST:
                summary: UntagMeeting
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_UntagResource.html">UntagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Untag
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK meeting resource.</p> <p>Applies the specified tags to the
                  specified Amazon Chime SDK meeting resource.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_UntagResource.html">UntagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
            /channels/{channelArn}/readMarker:
              PUT:
                summary: UpdateChannelReadMarker
                description: >-
                  <p>The details of the time when a user last read messages in a
                  channel.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannelReadMarker.html">UpdateChannelReadMarker</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Read
                  - Marker
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
            /sip-media-applications/{sipMediaApplicationId}/calls/{transactionId}:
              POST:
                summary: UpdateSipMediaApplicationCall
                description: >-
                  <p>Invokes the AWS Lambda function associated with the SIP
                  media application and transaction ID in an update request. The
                  Lambda function can then return a new set of actions.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipMediaApplicationCall.html">UpdateSipMediaApplicationCall</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
                  - Transactions
            /emergency-calling/address:
              POST:
                summary: ValidateE911Address
                description: >-
                  <p>Validates an address to be used for 911 calls made with
                  Amazon Chime Voice Connectors. You can use validated addresses
                  in a Presence Information Data Format Location Object file
                  that you include in SIP requests. That helps ensure that
                  addresses are routed to the appropriate Public Safety
                  Answering Point.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ValidateE911Address.html">ValidateE911Address</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </
                tags:
                  - Validate
                  - E911
                  - Addresses
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
                  - Transactions
                  - Addresses''
    overlays:
      - type: APIs.io Search
        url: overlays/chime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime
  - name: chime-sdk-identity
    description: >-
      <p>The Amazon Chime SDK Identity APIs in this section allow software
      developers to create and manage unique instances of their messaging
      applications. These APIs provide the overarching framework for creating
      and sending messages. For more information about the identity APIs, refer
      to <a
      href="https://docs.aws.amazon.com/chime/latest/APIReference/API_Operations_Amazon_Chime_SDK_Identity.html">Amazon
      Chime SDK identity</a>.</p>
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
            title: chime-sdk-identity
          paths:
            /app-instances:
              GET:
                summary: ListAppInstances
                description: >-
                  <p>Lists all Amazon Chime <code>AppInstance</code>s created
                  under a single AWS account.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Applications
                  - Instances
            /app-instances/{appInstanceArn}/admins:
              GET:
                summary: ListAppInstanceAdmins
                description: >-
                  <p>Returns a list of the administrators in the
                  <code>AppInstance</code>.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Administrator
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
            /app-instance-bots:
              GET:
                summary: ListAppInstanceBots
                description: >-
                  <p>Lists all <code>AppInstanceBots</code> created under a
                  single <code>AppInstance</code>.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Bots
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
            /app-instance-users:
              GET:
                summary: ListAppInstanceUsers
                description: >-
                  <p>List all <code>AppInstanceUsers</code> created under a
                  single <code>AppInstance</code>.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Users
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
            /app-instances/{appInstanceArn}:
              PUT:
                summary: UpdateAppInstance
                description: <p>Updates <code>AppInstance</code> metadata.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
            /app-instances/{appInstanceArn}/admins/{appInstanceAdminArn}:
              GET:
                summary: DescribeAppInstanceAdmin
                description: >-
                  <p>Returns the full details of an
                  <code>AppInstanceAdmin</code>.</p>
                tags:
                  - Describe
                  - Applications
                  - Instances
                  - Administrative
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
            /app-instance-bots/{appInstanceBotArn}:
              PUT:
                summary: UpdateAppInstanceBot
                description: >-
                  <p>Updates the name and metadata of an
                  <code>AppInstanceBot</code>.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Bot
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
            /app-instance-users/{appInstanceUserArn}:
              PUT:
                summary: UpdateAppInstanceUser
                description: >-
                  <p>Updates the details of an <code>AppInstanceUser</code>. You
                  can update names and metadata.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
            /app-instance-users/{appInstanceUserArn}/endpoints/{endpointId}:
              PUT:
                summary: UpdateAppInstanceUserEndpoint
                description: >-
                  <p>Updates the details of an
                  <code>AppInstanceUserEndpoint</code>. You can update the name
                  and <code>AllowMessage</code> values.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Endpoints
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
            /app-instances/{appInstanceArn}/retention-settings:
              PUT:
                summary: PutAppInstanceRetentionSettings
                description: >-
                  <p>Sets the amount of time in days that a given
                  <code>AppInstance</code> retains data.</p>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Retention
                  - Settings
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
            /app-instance-users/{appInstanceUserArn}/endpoints:
              POST:
                summary: RegisterAppInstanceUserEndpoint
                description: >-
                  <p>Registers an endpoint under an Amazon Chime
                  <code>AppInstanceUser</code>. The endpoint receives messages
                  for a user. For push notifications, the endpoint is a mobile
                  device used to receive mobile push notifications for a
                  user.</p>
                tags:
                  - Register
                  - Applications
                  - Instances
                  - Users
                  - Endpoints
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
            /tags:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK identity
                  resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
            /app-instance-users/{appInstanceUserArn}/expiration-settings:
              PUT:
                summary: PutAppInstanceUserExpirationSettings
                description: >-
                  <p>Sets the number of days before the
                  <code>AppInstanceUser</code> is automatically deleted.</p>
                  <note> <p>A background process deletes expired
                  <code>AppInstanceUsers</code> within 6 hours of expiration.
                  Actual deletion times may vary.</p> <p>Expired
                  <code>AppInstanceUsers</code> that have not yet been deleted
                  appear as active, and you can update their expiration
                  settings. The system honors the new settings.</p> </note>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Users
                  - Expiration
                  - Settings
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
                  - Expiration
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK identity resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
                  - Expiration
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes the specified tags from the specified Amazon Chime
                  SDK identity res
                tags:
                  - Untag
                  - Resources
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
                  - Expiration
                  - Tags
                  - Resources
                  - Tags
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-identity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-identity-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-identity
  - name: detective
    description: >-
      <p>Detective uses machine learning and purpose-built visualizations to
      help you to analyze and investigate security issues across your Amazon Web
      Services (Amazon Web Services) workloads. Detective automatically extracts
      time-based events such as login attempts, API calls, and network traffic
      from CloudTrail and Amazon Virtual Private Cloud (Amazon VPC) flow logs.
      It also extracts findings detected by Amazon GuardDuty.</p> <p>The
      Detective API primarily supports the creation and management of behavior
      graphs. A behavior graph contains the extracted data from a set of member
      accounts, and is created and managed by an administrator account.</p>
      <p>To add a member account to the behavior graph, the administrator
      account sends an invitation to the account. When the account accepts the
      invitation, it becomes a member account in the behavior graph.</p>
      <p>Detective is also integrated with Organizations. The organization
      management account designates the Detective administrator account for the
      organization. That account becomes the administrator account for the
      organization behavior graph. The Detective administrator account is also
      the delegated administrator account for Detective in Organizations.</p>
      <p>The Detective administrator account can enable any organization account
      as a member account in the organization behavior graph. The organization
      accounts do not receive invitations. The Detective administrator account
      can also invite other accounts to the organization behavior graph.</p>
      <p>Every behavior graph is specific to a Region. You can only use the API
      to manage behavior graphs that belong to the Region that is associated
      with the currently selected endpoint.</p> <p>The administrator account for
      a behavior graph can use the Detective API to do the following:</p> <ul>
      <li> <p>Enable and disable Detective. Enabling Detective creates a new
      behavior graph.</p> </li> <li> <p>View the list of member accounts in a
      behavior graph.</p> </li> <li> <p>Add member accounts to a behavior
      graph.</p> </li> <li> <p>Remove member accounts from a behavior graph.</p>
      </li> <li> <p>Apply tags to a behavior graph.</p> </li> </ul> <p>The
      organization management account can use the Detective API to select the
      delegated administrator for Detective.</p> <p>The Detective administrator
      account for an organization can use the Detective API to do the
      following:</p> <ul> <li> <p>Perform all of the functions of an
      administrator account.</p> </li> <li> <p>Determine whether to
      automatically enable new organization accounts as member accounts in the
      organization behavior graph.</p> </li> </ul> <p>An invited member account
      can use the Detective API to do the following:</p> <ul> <li> <p>View the
      list of behavior graphs that they are invited to.</p> </li> <li> <p>Accept
      an invitation to contribute to a behavior graph.</p> </li> <li> <p>Decline
      an invitation to contribute to a behavior graph.</p> </li> <li> <p>Remove
      their account from a behavior graph.</p> </li> </ul> <p>All API actions
      are logged as CloudTrail events. See <a
      href="https://docs.aws.amazon.com/detective/latest/adminguide/logging-using-cloudtrail.html">Logging
      Detective API Calls with CloudTrail</a>.</p> <note> <p>We replaced the
      term "master account" with the term "administrator account." An
      administrator account is used to centrally manage multiple accounts. In
      the case of Detective, the administrator account manages the accounts in
      their behavior graph.</p> </note>
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
            title: detective
          paths:
            /invitation:
              PUT:
                summary: AcceptInvitation
                description: >-
                  <p>Accepts an invitation for the member account to contribute
                  data to a behavior graph. This operation can only be called by
                  an invited member account. </p> <p>The request provides the
                  ARN of behavior graph.</p> <p>The member account status in the
                  graph must be <code>INVITED</code>.</p>
                tags:
                  - Accept
                  - Invitation
                  - Invitation
            /graph/datasources/get:
              POST:
                summary: BatchGetGraphMemberDatasources
                description: >-
                  <p>Gets data source package information for the behavior
                  graph.</p>
                tags:
                  - Batches
                  - Get
                  - Graphs
                  - Members
                  - Data Source
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
            /membership/datasources/get:
              POST:
                summary: BatchGetMembershipDatasources
                description: >-
                  <p>Gets information on the data source package history for an
                  account.</p>
                tags:
                  - Batches
                  - Get
                  - Membership
                  - Data Source
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
            /graph:
              POST:
                summary: CreateGraph
                description: >-
                  <p>Creates a new behavior graph for the calling account, and
                  sets that account as the administrator account. This operation
                  is called by the account that is enabling Detective.</p>
                  <p>Before you try to enable Detective, make sure that your
                  account has been enrolled in Amazon GuardDuty for at least 48
                  hours. If you do not meet this requirement, you cannot enable
                  Detective. If you do meet the GuardDuty prerequisite, then
                  when you make the request to enable Detective, it checks
                  whether your data volume is within the Detective quota. If it
                  exceeds the quota, then you cannot enable Detective. </p>
                  <p>The operation also enables Detective for the calling
                  account in the currently selected Region. It returns the ARN
                  of the new behavior graph.</p> <p> <code>CreateGraph</code>
                  triggers a process to create the corresponding data tables for
                  the new behavior graph.</p> <p>An account can only be the
                  administrator account for one behavior graph within a Region.
                  If the same account calls <code>CreateGraph</code> with the
                  same administrator account, it always returns the same
                  behavior graph ARN. It does not create a new behavior
                  graph.</p>
                tags:
                  - Create
                  - Graphs
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
            /graph/members:
              POST:
                summary: CreateMembers
                description: >-
                  <p> <code>CreateMembers</code> is used to send invitations to
                  accounts. For the organization behavior graph, the Detective
                  administrator account uses <code>CreateMembers</code> to
                  enable organization accounts as member accounts.</p> <p>For
                  invited accounts, <code>CreateMembers</code> sends a request
                  to invite the specified Amazon Web Services accounts to be
                  member accounts in the behavior graph. This operation can only
                  be called by the administrator account for a behavior graph.
                  </p> <p> <code>CreateMembers</code> verifies the accounts and
                  then invites the verified accounts. The administrator can
                  optionally specify to not send invitation emails to the member
                  accounts. This would be used when the administrator manages
                  their member accounts centrally.</p> <p>For organization
                  accounts in the organization behavior graph,
                  <code>CreateMembers</code> attempts to enable the accounts.
                  The organization accounts do not receive invitations.</p>
                  <p>The request provides the behavior graph ARN and the list of
                  accounts to invite or to enable.</p> <p>The response separates
                  the requested accounts into two lists:</p> <ul> <li> <p>The
                  accounts that <code>CreateMembers</code> was able to process.
                  For invited accounts, includes member accounts that are being
                  verified, that have passed verification and are to be invited,
                  and that have failed verification. For organization accounts
                  in the organization behavior graph, includes accounts that can
                  be enabled and that cannot be enabled.</p> </li> <li> <p>The
                  accounts that <code>CreateMembers</code> was unable to
                  process. This list includes accounts that were already invited
                  to be member accounts in the behavior graph.</p> </li> </ul>
                tags:
                  - Create
                  - Members
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
            /graph/removal:
              POST:
                summary: DeleteGraph
                description: >-
                  <p>Disables the specified behavior graph and queues it to be
                  deleted. This operation removes the behavior graph from each
                  member account's list of behavior graphs.</p> <p>
                  <code>DeleteGraph</code> can only be called by the
                  administrator account for a behavior graph.</p>
                tags:
                  - Delete
                  - Graphs
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
            /graph/members/removal:
              POST:
                summary: DeleteMembers
                description: >-
                  <p>Removes the specified member accounts from the behavior
                  graph. The removed accounts no longer contribute data to the
                  behavior graph. This operation can only be called by the
                  administrator account for the behavior graph.</p> <p>For
                  invited accounts, the removed accounts are deleted from the
                  list of accounts in the behavior graph. To restore the
                  account, the administrator account must send another
                  invitation.</p> <p>For organization accounts in the
                  organization behavior graph, the Detective administrator
                  account can always enable the organization account again.
                  Organization accounts that are not enabled as member accounts
                  are not included in the <code>ListMembers</code> results for
                  the organization behavior graph.</p> <p>An administrator
                  account cannot use <code>DeleteMembers</code> to remove their
                  own account from the behavior graph. To disable a behavior
                  graph, the administrator account uses the
                  <code>DeleteGraph</code> API method.</p>
                tags:
                  - Delete
                  - Members
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
            /orgs/describeOrganizationConfiguration:
              POST:
                summary: DescribeOrganizationConfiguration
                description: >-
                  <p>Returns information about the configuration for the
                  organization behavior graph. Currently indicates whether to
                  automatically enable new organization accounts as member
                  accounts.</p> <p>Can only be called by the Detective
                  administrator account for the organization. </p>
                tags:
                  - Describe
                  - Organizations
                  - Configurations
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
            /orgs/disableAdminAccount:
              POST:
                summary: DisableOrganizationAdminAccount
                description: >-
                  <p>Removes the Detective administrator account in the current
                  Region. Deletes the organization behavior graph.</p> <p>Can
                  only be called by the organization management account.</p>
                  <p>Removing the Detective administrator account does not
                  affect the delegated administrator account for Detective in
                  Organizations.</p> <p>To remove the delegated administrator
                  account in Organizations, use the Organizations API. Removing
                  the delegated administrator account also removes the Detective
                  administrator account in all Regions, except for Regions where
                  the Detective administrator account is the organization
                  management account.</p>
                tags:
                  - Disable
                  - Organizations
                  - Administrative
                  - Account
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
            /membership/removal:
              POST:
                summary: DisassociateMembership
                description: >-
                  <p>Removes the member account from the specified behavior
                  graph. This operation can only be called by an invited member
                  account that has the <code>ENABLED</code> status.</p> <p>
                  <code>DisassociateMembership</code> cannot be called by an
                  organization account in the organization behavior graph. For
                  the organization behavior graph, the Detective administrator
                  account determines which organization accounts to enable or
                  disable as member accounts.</p>
                tags:
                  - Disassociate
                  - Membership
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
            /orgs/enableAdminAccount:
              POST:
                summary: EnableOrganizationAdminAccount
                description: >-
                  <p>Designates the Detective administrator account for the
                  organization in the current Region.</p> <p>If the account does
                  not have Detective enabled, then enables Detective for that
                  account and creates a new behavior graph.</p> <p>Can only be
                  called by the organization management account.</p> <p>If the
                  organization has a delegated administrator account in
                  Organizations, then the Detective administrator account must
                  be either the delegated administrator account or the
                  organization management account.</p> <p>If the organization
                  does not have a delegated administrator account in
                  Organizations, then you can choose any account in the
                  organization. If you choose an account other than the
                  organization management account, Detective calls Organizations
                  to make that account the delegated administrator account for
                  Detective. The organization management account cannot be the
                  delegated administrator account.</p>
                tags:
                  - Enable
                  - Organizations
                  - Administrative
                  - Account
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
            /investigations/getInvestigation:
              POST:
                summary: GetInvestigation
                description: >-
                  <p>Returns the investigation results of an investigation for a
                  behavior graph. </p>
                tags:
                  - Get
                  - Investigations
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
            /graph/members/get:
              POST:
                summary: GetMembers
                description: >-
                  <p>Returns the membership details for specified member
                  accounts for a behavior graph.</p>
                tags:
                  - Get
                  - Members
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
            /graph/datasources/list:
              POST:
                summary: ListDatasourcePackages
                description: <p>Lists data source packages in the behavior graph.</p>
                tags:
                  - Lists
                  - Data Source
                  - Packages
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
            /graphs/list:
              POST:
                summary: ListGraphs
                description: >-
                  <p>Returns the list of behavior graphs that the calling
                  account is an administrator account of. This operation can
                  only be called by an administrator account.</p> <p>Because an
                  account can currently only be the administrator of one
                  behavior graph within a Region, the results always contain a
                  single behavior graph.</p>
                tags:
                  - Lists
                  - Graphs
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
            /investigations/listIndicators:
              POST:
                summary: ListIndicators
                description: <p>Get the indicators from an investigation</p>
                tags:
                  - Lists
                  - Indicators
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
            /investigations/listInvestigations:
              POST:
                summary: ListInvestigations
                description: <p>List all Investigations.</p>
                tags:
                  - Lists
                  - Investigations
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
            /invitations/list:
              POST:
                summary: ListInvitations
                description: >-
                  <p>Retrieves the list of open and accepted behavior graph
                  invitations for the member account. This operation can only be
                  called by an invited member account.</p> <p>Open invitations
                  are invitations that the member account has not responded
                  to.</p> <p>The results do not include behavior graphs for
                  which the member account declined the invitation. The results
                  also do not include behavior graphs that the member account
                  resigned from or was removed from.</p>
                tags:
                  - Lists
                  - Invitations
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
            /graph/members/list:
              POST:
                summary: ListMembers
                description: >-
                  <p>Retrieves the list of member accounts for a behavior
                  graph.</p> <p>For invited accounts, the results do not include
                  member accounts that were removed from the behavior graph.</p>
                  <p>For the organization behavior graph, the results do not
                  include organization accounts that the Detective administrator
                  account has not enabled as member accounts.</p>
                tags:
                  - Lists
                  - Members
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
            /orgs/adminAccountslist:
              POST:
                summary: ListOrganizationAdminAccounts
                description: >-
                  <p>Returns information about the Detective administrator
                  account for an organization. Can only be called by the
                  organization management account.</p>
                tags:
                  - Lists
                  - Organizations
                  - Administrative
                  - Accounts
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a behavior graph.</p>
                tags:
                  - Untag
                  - Resources
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
            /invitation/removal:
              POST:
                summary: RejectInvitation
                description: >-
                  <p>Rejects an invitation to contribute the account data to a
                  behavior graph. This operation must be called by an invited
                  member account that has the <code>INVITED</code> status.</p>
                  <p> <code>RejectInvitation</code> cannot be called by an
                  organization account in the organization behavior graph. In
                  the organization behavior graph, organization accounts do not
                  receive an invitation.</p>
                tags:
                  - Reject
                  - Invitation
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
            /investigations/startInvestigation:
              POST:
                summary: StartInvestigation
                description: <p>initiate an investigation on an entity in a graph</p>
                tags:
                  - Start
                  - Investigations
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
            /graph/member/monitoringstate:
              POST:
                summary: StartMonitoringMember
                description: >-
                  <p>Sends a request to enable data ingest for a member account
                  that has a status of <code>ACCEPTED_BUT_DISABLED</code>.</p>
                  <p>For valid member accounts, the status is updated as
                  follows.</p> <ul> <li> <p>If Detective enabled the member
                  account, then the new status is <code>ENABLED</code>.</p>
                  </li> <li> <p>If Detective cannot enable the member account,
                  the status remains <code>ACCEPTED_BUT_DISABLED</code>. </p>
                  </li> </ul>
                tags:
                  - Start
                  - Monitoring
                  - Members
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
                  - Members
                  - Monitoring State
            /graph/datasources/update:
              POST:
                summary: UpdateDatasourcePackages
                description: <p>Starts a data source packages for the behavior graph.</p>
                tags:
                  - Update
                  - Data Source
                  - Packages
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
                  - Members
                  - Monitoring State
                  - Update
            /investigations/updateInvestigationState:
              POST:
                summary: UpdateInvestigationState
                description: <p>Update the state of an investigation.</p>
                tags:
                  - Update
                  - Investigations
                  - States
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
                  - Members
                  - Monitoring State
                  - Update
                  - States
            /orgs/updateOrganizationConfiguration:
              POST:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the configuration for the Organizations integration
                  in the current Region. Can only be called by the Detective
                  administrator account for the organiz
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Invitation
                  - Graphs
                  - Data Source
                  - Get
                  - Membership
                  - Members
                  - Removal
                  - Organizations
                  - Configurations
                  - Administrative
                  - Account
                  - Investigations
                  - Lists
                  - Graphs
                  - Indicators
                  - Investigations
                  - Invitations
                  - Accounts List
                  - Resources
                  - ARN
                  - Members
                  - Monitoring State
                  - Update
                  - Sta
    overlays:
      - type: APIs.io Search
        url: overlays/detective-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/detective-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:detective
  - name: guardduty
    description: >-
      <p>Amazon GuardDuty is a continuous security monitoring service that
      analyzes and processes the following foundational data sources - VPC flow
      logs, Amazon Web Services CloudTrail management event logs, CloudTrail S3
      data event logs, EKS audit logs, DNS logs, Amazon EBS volume data, runtime
      activity belonging to container workloads, such as Amazon EKS, Amazon ECS
      (including Amazon Web Services Fargate), and Amazon EC2 instances. It uses
      threat intelligence feeds, such as lists of malicious IPs and domains, and
      machine learning to identify unexpected, potentially unauthorized, and
      malicious activity within your Amazon Web Services environment. This can
      include issues like escalations of privileges, uses of exposed
      credentials, or communication with malicious IPs, domains, or presence of
      malware on your Amazon EC2 instances and container workloads. For example,
      GuardDuty can detect compromised EC2 instances and container workloads
      serving malware, or mining bitcoin. </p> <p>GuardDuty also monitors Amazon
      Web Services account access behavior for signs of compromise, such as
      unauthorized infrastructure deployments like EC2 instances deployed in a
      Region that has never been used, or unusual API calls like a password
      policy change to reduce password strength. </p> <p>GuardDuty informs you
      about the status of your Amazon Web Services environment by producing
      security findings that you can view in the GuardDuty console or through
      Amazon EventBridge. For more information, see the <i> <a
      href="https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html">Amazon
      GuardDuty User Guide</a> </i>. </p>
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
            title: guardduty
          paths:
            /detector/{detectorId}/administrator:
              GET:
                summary: GetAdministratorAccount
                description: >-
                  <p>Provides the details of the GuardDuty administrator account
                  associated with the current GuardDuty member account.</p>
                  <note> <p>If the organization's management account or a
                  delegated administrator runs this API, it will return success
                  (<code>HTTP 200</code>) but no content.</p> </note>
                tags:
                  - Get
                  - Administrator
                  - Account
                  - Identifiers
                  - Administrator
            /detector/{detectorId}/master:
              GET:
                summary: GetMasterAccount
                description: >-
                  <p>Provides the details for the GuardDuty administrator
                  account associated with the current GuardDuty member
                  account.</p>
                tags:
                  - Get
                  - Master
                  - Account
                  - Identifiers
                  - Administrator
                  - Master
            /detector/{detectorId}/findings/archive:
              POST:
                summary: ArchiveFindings
                description: >-
                  <p>Archives GuardDuty findings that are specified by the list
                  of finding IDs.</p> <note> <p>Only the administrator account
                  can archive findings. Member accounts don't have permission to
                  archive findings from their accounts.</p> </note>
                tags:
                  - Archive
                  - Findings
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
            /detector:
              GET:
                summary: ListDetectors
                description: >-
                  <p>Lists detectorIds of all the existing Amazon GuardDuty
                  detector resources.</p>
                tags:
                  - Lists
                  - Detectors
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
            /detector/{detectorId}/filter:
              GET:
                summary: ListFilters
                description: <p>Returns a paginated list of the current filters.</p>
                tags:
                  - Lists
                  - Filters
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
            /detector/{detectorId}/ipset:
              GET:
                summary: ListIPSets
                description: >-
                  <p>Lists the IPSets of the GuardDuty service specified by the
                  detector ID. If you use this operation from a member account,
                  the IPSets returned are the IPSets from the associated
                  administrator account.</p>
                tags:
                  - Lists
                  - Sets
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
            /detector/{detectorId}/member:
              GET:
                summary: ListMembers
                description: >-
                  <p>Lists details about all member accounts for the current
                  GuardDuty administrator account.</p>
                tags:
                  - Lists
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
            /detector/{detectorId}/publishingDestination:
              GET:
                summary: ListPublishingDestinations
                description: >-
                  <p>Returns a list of publishing destinations associated with
                  the specified <code>detectorId</code>.</p>
                tags:
                  - Lists
                  - Publishing
                  - Destinations
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
            /detector/{detectorId}/findings/create:
              POST:
                summary: CreateSampleFindings
                description: >-
                  <p>Generates sample findings of types specified by the list of
                  finding types. If 'NULL' is specified for
                  <code>findingTypes</code>, the API generates sample findings
                  of all supported finding types.</p>
                tags:
                  - Create
                  - Samples
                  - Findings
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
            /detector/{detectorId}/threatintelset:
              GET:
                summary: ListThreatIntelSets
                description: >-
                  <p>Lists the ThreatIntelSets of the GuardDuty service
                  specified by the detector ID. If you use this operation from a
                  member account, the ThreatIntelSets associated with the
                  administrator account are returned.</p>
                tags:
                  - Lists
                  - Threat
                  - Intelligence
                  - Sets
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
            /invitation/decline:
              POST:
                summary: DeclineInvitations
                description: >-
                  <p>Declines invitations sent to the current member account by
                  Amazon Web Services accounts specified by their account
                  IDs.</p>
                tags:
                  - Decline
                  - Invitations
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
            /detector/{detectorId}:
              POST:
                summary: UpdateDetector
                description: >-
                  <p>Updates the Amazon GuardDuty detector specified by the
                  detectorId.</p> <p>There might be regional differences because
                  some data sources might not be available in all the Amazon Web
                  Services Regions where GuardDuty is presently supported. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_regions.html">Regions
                  and endpoints</a>.</p>
                tags:
                  - Update
                  - Detectors
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
            /detector/{detectorId}/filter/{filterName}:
              POST:
                summary: UpdateFilter
                description: <p>Updates the filter specified by the filter name.</p>
                tags:
                  - Update
                  - Filter
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
            /detector/{detectorId}/ipset/{ipSetId}:
              POST:
                summary: UpdateIPSet
                description: <p>Updates the IPSet specified by the IPSet ID.</p>
                tags:
                  - Update
                  - Sets
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
            /invitation/delete:
              POST:
                summary: DeleteInvitations
                description: >-
                  <p>Deletes invitations sent to the current member account by
                  Amazon Web Services accounts specified by their account
                  IDs.</p>
                tags:
                  - Delete
                  - Invitations
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
            /detector/{detectorId}/member/delete:
              POST:
                summary: DeleteMembers
                description: >-
                  <p>Deletes GuardDuty member accounts (to the current GuardDuty
                  administrator account) specified by the account IDs.</p>
                  <p>With <code>autoEnableOrganizationMembers</code>
                  configuration for your organization set to <code>ALL</code>,
                  you'll receive an error if you attempt to disable GuardDuty
                  for a member account in your organization.</p>
                tags:
                  - Delete
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
            /detector/{detectorId}/publishingDestination/{destinationId}:
              POST:
                summary: UpdatePublishingDestination
                description: >-
                  <p>Updates information about the publishing destination
                  specified by the <code>destinationId</code>.</p>
                tags:
                  - Update
                  - Publishing
                  - Destinations
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
            /detector/{detectorId}/threatintelset/{threatIntelSetId}:
              POST:
                summary: UpdateThreatIntelSet
                description: >-
                  <p>Updates the ThreatIntelSet specified by the ThreatIntelSet
                  ID.</p>
                tags:
                  - Update
                  - Threat
                  - Intelligence
                  - Sets
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
            /detector/{detectorId}/malware-scans:
              POST:
                summary: DescribeMalwareScans
                description: >-
                  <p>Returns a list of malware scans. Each member account can
                  view the malware scans for their own accounts. An
                  administrator can view the malware scans for all the member
                  accounts.</p> <p>There might be regional differences because
                  some data sources might not be available in all the Amazon Web
                  Services Regions where GuardDuty is presently supported. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_regions.html">Regions
                  and endpoints</a>.</p>
                tags:
                  - Describe
                  - Malware
                  - Scans
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
            /detector/{detectorId}/admin:
              POST:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Configures the delegated administrator account with the
                  provided values. You must provide a value for either
                  <code>autoEnableOrganizationMembers</code> or
                  <code>autoEnable</code>, but not both. </p> <p>There might be
                  regional differences because some data sources might not be
                  available in all the Amazon Web Services Regions where
                  GuardDuty is presently supported. For more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_regions.html">Regions
                  and endpoints</a>.</p>
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
            /admin/disable:
              POST:
                summary: DisableOrganizationAdminAccount
                description: >-
                  <p>Removes the existing GuardDuty delegated administrator of
                  the organization. Only the organization's management account
                  can run this API operation.</p>
                tags:
                  - Disable
                  - Organizations
                  - Administrative
                  - Account
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
            /detector/{detectorId}/administrator/disassociate:
              POST:
                summary: DisassociateFromAdministratorAccount
                description: >-
                  <p>Disassociates the current GuardDuty member account from its
                  administrator account.</p> <p>When you disassociate an invited
                  member from a GuardDuty delegated administrator, the member
                  account details obtained from the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_CreateMembers.html">CreateMembers</a>
                  API, including the associated email addresses, are retained.
                  This is done so that the delegated administrator can invoke
                  the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_InviteMembers.html">InviteMembers</a>
                  API without the need to invoke the CreateMembers API again. To
                  remove the details associated with a member account, the
                  delegated administrator must invoke the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_DeleteMembers.html">DeleteMembers</a>
                  API. </p> <p>With <code>autoEnableOrganizationMembers</code>
                  configuration for your organization set to <code>ALL</code>,
                  you'll receive an error if you attempt to disable GuardDuty in
                  a member account.</p>
                tags:
                  - Disassociate
                  - From
                  - Administrator
                  - Account
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
            /detector/{detectorId}/master/disassociate:
              POST:
                summary: DisassociateFromMasterAccount
                description: >-
                  <p>Disassociates the current GuardDuty member account from its
                  administrator account.</p> <p>When you disassociate an invited
                  member from a GuardDuty delegated administrator, the member
                  account details obtained from the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_CreateMembers.html">CreateMembers</a>
                  API, including the associated email addresses, are retained.
                  This is done so that the delegated administrator can invoke
                  the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_InviteMembers.html">InviteMembers</a>
                  API without the need to invoke the CreateMembers API again. To
                  remove the details associated with a member account, the
                  delegated administrator must invoke the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_DeleteMembers.html">DeleteMembers</a>
                  API.</p>
                tags:
                  - Disassociate
                  - From
                  - Master
                  - Account
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
            /detector/{detectorId}/member/disassociate:
              POST:
                summary: DisassociateMembers
                description: >-
                  <p>Disassociates GuardDuty member accounts (from the current
                  administrator account) specified by the account IDs.</p>
                  <p>When you disassociate an invited member from a GuardDuty
                  delegated administrator, the member account details obtained
                  from the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_CreateMembers.html">CreateMembers</a>
                  API, including the associated email addresses, are retained.
                  This is done so that the delegated administrator can invoke
                  the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_InviteMembers.html">InviteMembers</a>
                  API without the need to invoke the CreateMembers API again. To
                  remove the details associated with a member account, the
                  delegated administrator must invoke the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_DeleteMembers.html">DeleteMembers</a>
                  API. </p> <p>With <code>autoEnableOrganizationMembers</code>
                  configuration for your organization set to <code>ALL</code>,
                  you'll receive an error if you attempt to disassociate a
                  member account before removing them from your
                  organization.</p>
                tags:
                  - Disassociate
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
            /admin/enable:
              POST:
                summary: EnableOrganizationAdminAccount
                description: >-
                  <p>Designates an Amazon Web Services account within the
                  organization as your GuardDuty delegated administrator. Only
                  the organization's management account can run this API
                  operation.</p>
                tags:
                  - Enable
                  - Organizations
                  - Administrative
                  - Account
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /detector/{detectorId}/coverage/statistics:
              POST:
                summary: GetCoverageStatistics
                description: >-
                  <p>Retrieves aggregated statistics for your account. If you
                  are a GuardDuty administrator, you can retrieve the statistics
                  for all the resources associated with the active member
                  accounts in your organization who have enabled Runtime
                  Monitoring and have the GuardDuty security agent running on
                  their resources.</p>
                tags:
                  - Get
                  - Coverage
                  - Statistics
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
            /detector/{detectorId}/findings/get:
              POST:
                summary: GetFindings
                description: >-
                  <p>Describes Amazon GuardDuty findings specified by finding
                  IDs.</p>
                tags:
                  - Get
                  - Findings
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
            /detector/{detectorId}/findings/statistics:
              POST:
                summary: GetFindingsStatistics
                description: >-
                  <p>Lists Amazon GuardDuty findings statistics for the
                  specified detector ID.</p>
                tags:
                  - Get
                  - Findings
                  - Statistics
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
            /invitation/count:
              GET:
                summary: GetInvitationsCount
                description: >-
                  <p>Returns the count of all GuardDuty membership invitations
                  that were sent to the current member account except the
                  currently accepted invitation.</p>
                tags:
                  - Get
                  - Invitations
                  - Count
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
            /detector/{detectorId}/malware-scan-settings:
              POST:
                summary: UpdateMalwareScanSettings
                description: >-
                  <p>Updates the malware scan settings.</p> <p>There might be
                  regional differences because some data sources might not be
                  available in all the Amazon Web Services Regions where
                  GuardDuty is presently supported. For more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_regions.html">Regions
                  and endpoints</a>.</p>
                tags:
                  - Update
                  - Malware
                  - Scans
                  - Settings
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
            /detector/{detectorId}/member/detector/get:
              POST:
                summary: GetMemberDetectors
                description: >-
                  <p>Describes which data sources are enabled for the member
                  account's detector.</p> <p>There might be regional differences
                  because some data sources might not be available in all the
                  Amazon Web Services Regions where GuardDuty is presently
                  supported. For more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_regions.html">Regions
                  and endpoints</a>.</p>
                tags:
                  - Get
                  - Members
                  - Detectors
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
            /detector/{detectorId}/member/get:
              POST:
                summary: GetMembers
                description: >-
                  <p>Retrieves GuardDuty member accounts (of the current
                  GuardDuty administrator account) specified by the account
                  IDs.</p>
                tags:
                  - Get
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
            /organization/statistics:
              GET:
                summary: GetOrganizationStatistics
                description: >-
                  <p>Retrieves how many active member accounts in your Amazon
                  Web Services organization have each feature enabled within
                  GuardDuty. Only a delegated GuardDuty administrator of an
                  organization can run this API.</p> <p>When you create a new
                  Amazon Web Services organization, it might take up to 24 hours
                  to generate the statistics for the entire organization.</p>
                tags:
                  - Get
                  - Organizations
                  - Statistics
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
            /detector/{detectorId}/freeTrial/daysRemaining:
              POST:
                summary: GetRemainingFreeTrialDays
                description: >-
                  <p>Provides the number of days left for each data source used
                  in the free trial period.</p>
                tags:
                  - Get
                  - Remaining
                  - Free
                  - Trials
                  - Days
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
            /detector/{detectorId}/usage/statistics:
              POST:
                summary: GetUsageStatistics
                description: >-
                  <p>Lists Amazon GuardDuty usage statistics over the last 30
                  days for the specified detector ID. For newly enabled
                  detectors or data sources, the cost returned will include only
                  the usage so far under 30 days. This may differ from the cost
                  metrics in the console, which project usage over 30 days to
                  provide a monthly cost estimate. For more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/monitoring_costs.html#usage-calculations">Understanding
                  How Usage Costs are Calculated</a>.</p>
                tags:
                  - Get
                  - Usage
                  - Statistics
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
            /detector/{detectorId}/member/invite:
              POST:
                summary: InviteMembers
                description: >-
                  <p>Invites Amazon Web Services accounts to become members of
                  an organization administered by the Amazon Web Services
                  account that invokes this API. If you are using Amazon Web
                  Services Organizations to manage your GuardDuty environment,
                  this step is not needed. For more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_organizations.html">Managing
                  accounts with organizations</a>.</p> <p>To invite Amazon Web
                  Services accounts, the first step is to ensure that GuardDuty
                  has been enabled in the potential member accounts. You can now
                  invoke this API to add accounts by invitation. The invited
                  accounts can either accept or decline the invitation from
                  their GuardDuty accounts. Each invited Amazon Web Services
                  account can choose to accept the invitation from only one
                  Amazon Web Services account. For more information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_invitations.html">Managing
                  GuardDuty accounts by invitation</a>.</p> <p>After the invite
                  has been accepted and you choose to disassociate a member
                  account (by using <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_DisassociateMembers.html">DisassociateMembers</a>)
                  from your account, the details of the member account obtained
                  by invoking <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_CreateMembers.html">CreateMembers</a>,
                  including the associated email addresses, will be retained.
                  This is done so that you can invoke InviteMembers without the
                  need to invoke <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_CreateMembers.html">CreateMembers</a>
                  again. To remove the details associated with a member account,
                  you must also invoke <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_DeleteMembers.html">DeleteMembers</a>.
                  </p>
                tags:
                  - Invite
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
            /detector/{detectorId}/coverage:
              POST:
                summary: ListCoverage
                description: >-
                  <p>Lists coverage details for your GuardDuty account. If
                  you're a GuardDuty administrator, you can retrieve all
                  resources associated with the active member accounts in your
                  organization.</p> <p>Make sure the accounts have Runtime
                  Monitoring enabled and GuardDuty agent running on their
                  resources.</p>
                tags:
                  - Lists
                  - Coverage
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
            /detector/{detectorId}/findings:
              POST:
                summary: ListFindings
                description: >-
                  <p>Lists Amazon GuardDuty findings for the specified detector
                  ID.</p>
                tags:
                  - Lists
                  - Findings
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
            /invitation:
              GET:
                summary: ListInvitations
                description: >-
                  <p>Lists all GuardDuty membership invitations that were sent
                  to the current Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Invitations
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
            /admin:
              GET:
                summary: ListOrganizationAdminAccounts
                description: >-
                  <p>Lists the accounts designated as GuardDuty delegated
                  administrators. Only the organization's management account can
                  run this API operation.</p>
                tags:
                  - Lists
                  - Organizations
                  - Administrative
                  - Accounts
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
            /malware-scan/start:
              POST:
                summary: StartMalwareScan
                description: >-
                  <p>Initiates the malware scan. Invoking this API will
                  automatically create the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/slr-permissions-malware-protection.html">Service-linked
                  role </a> in the corresponding account.</p>
                tags:
                  - Start
                  - Malware
                  - Scans
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
                  - Start
            /detector/{detectorId}/member/start:
              POST:
                summary: StartMonitoringMembers
                description: >-
                  <p>Turns on GuardDuty monitoring of the specified member
                  accounts. Use this operation to restart monitoring of accounts
                  that you stopped monitoring with the <a
                  href="https://docs.aws.amazon.com/guardduty/latest/APIReference/API_StopMonitoringMembers.html">StopMonitoringMembers</a>
                  operation.</p>
                tags:
                  - Start
                  - Monitoring
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
                  - Start
            /detector/{detectorId}/member/stop:
              POST:
                summary: StopMonitoringMembers
                description: >-
                  <p>Stops GuardDuty monitoring for the specified member
                  accounts. Use the <code>StartMonitoringMembers</code>
                  operation to restart monitoring for those accounts.</p>
                  <p>With <code>autoEnableOrganizationMembers</code>
                  configuration for your organization set to <code>ALL</code>,
                  you'll receive an error if you attempt to stop monitoring the
                  member accounts in your organization.</p>
                tags:
                  - Stop
                  - Monitoring
                  - Members
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
                  - Start
                  - Stop
            /detector/{detectorId}/findings/unarchive:
              POST:
                summary: UnarchiveFindings
                description: >-
                  <p>Unarchives GuardDuty findings specified by the
                  <code>findingIds</code>.</p>
                tags:
                  - Unarchive
                  - Findings
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
                  - Start
                  - Stop
                  - Unarchive
            /detector/{detectorId}/findings/feedback:
              POST:
                summary: UpdateFindingsFeedback
                description: >-
                  <p>Marks the specified GuardDuty findings as useful or not
                  useful.</p>
                tags:
                  - Update
                  - Findings
                  - Feedback
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
                  - Start
                  - Stop
                  - Unarchive
                  - Feedback
            /detector/{detectorId}/member/detector/update:
              POST:
                summary: UpdateMemberDetectors
                description: >-
                  <p>Contains information on member accounts to be updated.</p>
                  <p>There might be regional differences because some data
                  sources might not be available in all the Amazon Web Services
                  Regions where GuardDuty is presently supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_regions.html">Regions
                  and endpoint
                tags:
                  - Update
                  - Members
                  - Detectors
                  - Identifiers
                  - Administrator
                  - Master
                  - Findings
                  - Archive
                  - Detectors
                  - Filter
                  - Ipset
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - Threatintelset
                  - Invitation
                  - Decline
                  - Names
                  - IP
                  - Sets
                  - Delete
                  - Threat
                  - Intelligence
                  - Malware
                  - Scans
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - Coverage
                  - Statistics
                  - Get
                  - Count
                  - Scans
                  - Settings
                  - Organizations
                  - Free
                  - Trials
                  - Days
                  - Remaining
                  - Usage
                  - Invite
                  - ARN
                  - Start
                  - Stop
                  - Unarchive
                  - Feedback
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/guardduty-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/guardduty-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:guardduty
  - name: inspector2
    description: >-
      <p>Amazon Inspector is a vulnerability discovery service that automates
      continuous scanning for security vulnerabilities within your Amazon EC2,
      Amazon ECR, and Amazon Web Services Lambda environments.</p>
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
            title: inspector2
          paths:
            /members/associate:
              POST:
                summary: AssociateMember
                description: >-
                  <p>Associates an Amazon Web Services account with an Amazon
                  Inspector delegated administrator. An HTTP 200 response
                  indicates the association was successfully started, but
                  doesn’t indicate whether it was completed. You can check if
                  the association completed by using <a
                  href="https://docs.aws.amazon.com/inspector/v2/APIReference/API_ListMembers.html">ListMembers</a>
                  for multiple accounts or <a
                  href="https://docs.aws.amazon.com/inspector/v2/APIReference/API_GetMember.html">GetMembers</a>
                  for a single account.</p>
                tags:
                  - Associate
                  - Members
                  - Members
                  - Associate
            /status/batch/get:
              POST:
                summary: BatchGetAccountStatus
                description: >-
                  <p>Retrieves the Amazon Inspector status of multiple Amazon
                  Web Services accounts within your environment.</p>
                tags:
                  - Batches
                  - Get
                  - Account
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
            /codesnippet/batchget:
              POST:
                summary: BatchGetCodeSnippet
                description: >-
                  <p>Retrieves code snippets from findings that Amazon Inspector
                  detected code vulnerabilities in.</p>
                tags:
                  - Batches
                  - Get
                  - Code
                  - Snippets
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
            /findings/details/batch/get:
              POST:
                summary: BatchGetFindingDetails
                description: <p>Gets vulnerability details for findings.</p>
                tags:
                  - Batches
                  - Get
                  - Findings
                  - Details
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
            /freetrialinfo/batchget:
              POST:
                summary: BatchGetFreeTrialInfo
                description: >-
                  <p>Gets free trial status for multiple Amazon Web Services
                  accounts.</p>
                tags:
                  - Batches
                  - Get
                  - Free
                  - Trials
                  - Info
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
            /ec2deepinspectionstatus/member/batch/get:
              POST:
                summary: BatchGetMemberEc2DeepInspectionStatus
                description: >-
                  <p>Retrieves Amazon Inspector deep inspection activation
                  status of multiple member accounts within your organization.
                  You must be the delegated administrator of an organization in
                  Amazon Inspector to use this API.</p>
                tags:
                  - Batches
                  - Get
                  - Members
                  - EC2
                  - Deep
                  - Inspections
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
            /ec2deepinspectionstatus/member/batch/update:
              POST:
                summary: BatchUpdateMemberEc2DeepInspectionStatus
                description: >-
                  <p>Activates or deactivates Amazon Inspector deep inspection
                  for the provided member accounts in your organization. You
                  must be the delegated administrator of an organization in
                  Amazon Inspector to use this API.</p>
                tags:
                  - Batches
                  - Update
                  - Members
                  - EC2
                  - Deep
                  - Inspections
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
            /reporting/cancel:
              POST:
                summary: CancelFindingsReport
                description: <p>Cancels the given findings report.</p>
                tags:
                  - Cancel
                  - Findings
                  - Reports
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
            /sbomexport/cancel:
              POST:
                summary: CancelSbomExport
                description: <p>Cancels a software bill of materials (SBOM) report.</p>
                tags:
                  - Cancel
                  - Sbom
                  - Export
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
            /cis/scan-configuration/create:
              POST:
                summary: CreateCisScanConfiguration
                description: <p>Creates a CIS scan configuration.</p>
                tags:
                  - Create
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
            /filters/create:
              POST:
                summary: CreateFilter
                description: >-
                  <p>Creates a filter resource using specified filter criteria.
                  When the filter action is set to <code>SUPPRESS</code> this
                  action creates a suppression rule.</p>
                tags:
                  - Create
                  - Filter
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
            /reporting/create:
              POST:
                summary: CreateFindingsReport
                description: >-
                  <p>Creates a finding report. By default only
                  <code>ACTIVE</code> findings are returned in the report. To
                  see <code>SUPRESSED</code> or <code>CLOSED</code> findings you
                  must specify a value for the <code>findingStatus</code> filter
                  criteria. </p>
                tags:
                  - Create
                  - Findings
                  - Reports
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
            /sbomexport/create:
              POST:
                summary: CreateSbomExport
                description: <p>Creates a software bill of materials (SBOM) report.</p>
                tags:
                  - Create
                  - Sbom
                  - Export
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
            /cis/scan-configuration/delete:
              POST:
                summary: DeleteCisScanConfiguration
                description: <p>Deletes a CIS scan configuration.</p>
                tags:
                  - Delete
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
            /filters/delete:
              POST:
                summary: DeleteFilter
                description: <p>Deletes a filter resource.</p>
                tags:
                  - Delete
                  - Filter
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
            /organizationconfiguration/describe:
              POST:
                summary: DescribeOrganizationConfiguration
                description: >-
                  <p>Describe Amazon Inspector configuration settings for an
                  Amazon Web Services organization.</p>
                tags:
                  - Describe
                  - Organizations
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
            /disable:
              POST:
                summary: Disable
                description: >-
                  <p>Disables Amazon Inspector scans for one or more Amazon Web
                  Services accounts. Disabling all scan types in an account
                  disables the Amazon Inspector service.</p>
                tags:
                  - Disable
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
            /delegatedadminaccounts/disable:
              POST:
                summary: DisableDelegatedAdminAccount
                description: >-
                  <p>Disables the Amazon Inspector delegated administrator for
                  your organization.</p>
                tags:
                  - Disable
                  - Delegated
                  - Administrative
                  - Account
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
            /members/disassociate:
              POST:
                summary: DisassociateMember
                description: >-
                  <p>Disassociates a member account from an Amazon Inspector
                  delegated administrator.</p>
                tags:
                  - Disassociate
                  - Members
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
            /enable:
              POST:
                summary: Enable
                description: >-
                  <p>Enables Amazon Inspector scans for one or more Amazon Web
                  Services accounts.</p>
                tags:
                  - Enable
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
            /delegatedadminaccounts/enable:
              POST:
                summary: EnableDelegatedAdminAccount
                description: >-
                  <p>Enables the Amazon Inspector delegated administrator for
                  your Organizations organization.</p>
                tags:
                  - Enable
                  - Delegated
                  - Administrative
                  - Account
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
            /cis/scan/report/get:
              POST:
                summary: GetCisScanReport
                description: <p>Retrieves a CIS scan report.</p>
                tags:
                  - Get
                  - ~~
                  - Scans
                  - Reports
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
            /cis/scan-result/details/get:
              POST:
                summary: GetCisScanResultDetails
                description: <p>Retrieves CIS scan result details.</p>
                tags:
                  - Get
                  - ~~
                  - Scans
                  - Results
                  - Details
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
            /configuration/get:
              POST:
                summary: GetConfiguration
                description: <p>Retrieves setting configurations for Inspector scans.</p>
                tags:
                  - Get
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
            /delegatedadminaccounts/get:
              POST:
                summary: GetDelegatedAdminAccount
                description: >-
                  <p>Retrieves information about the Amazon Inspector delegated
                  administrator for your organization.</p>
                tags:
                  - Get
                  - Delegated
                  - Administrative
                  - Account
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
            /ec2deepinspectionconfiguration/get:
              POST:
                summary: GetEc2DeepInspectionConfiguration
                description: >-
                  <p>Retrieves the activation status of Amazon Inspector deep
                  inspection and custom paths associated with your account. </p>
                tags:
                  - Get
                  - EC2
                  - Deep
                  - Inspections
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
            /encryptionkey/get:
              GET:
                summary: GetEncryptionKey
                description: <p>Gets an encryption key.</p>
                tags:
                  - Get
                  - Encryption
                  - Keys
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /reporting/status/get:
              POST:
                summary: GetFindingsReportStatus
                description: <p>Gets the status of a findings report.</p>
                tags:
                  - Get
                  - Findings
                  - Reports
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /members/get:
              POST:
                summary: GetMember
                description: <p>Gets member information for your organization.</p>
                tags:
                  - Get
                  - Members
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /sbomexport/get:
              POST:
                summary: GetSbomExport
                description: >-
                  <p>Gets details of a software bill of materials (SBOM)
                  report.</p>
                tags:
                  - Get
                  - Sbom
                  - Export
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /accountpermissions/list:
              POST:
                summary: ListAccountPermissions
                description: >-
                  <p>Lists the permissions an account has to configure Amazon
                  Inspector.</p>
                tags:
                  - Lists
                  - Account
                  - Permissions
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
            /cis/scan-configuration/list:
              POST:
                summary: ListCisScanConfigurations
                description: <p>Lists CIS scan configurations.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
            /cis/scan-result/check/list:
              POST:
                summary: ListCisScanResultsAggregatedByChecks
                description: <p>Lists scan results aggregated by checks.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Results
                  - Aggregated
                  - By
                  - Checks
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
            /cis/scan-result/resource/list:
              POST:
                summary: ListCisScanResultsAggregatedByTargetResource
                description: <p>Lists scan results aggregated by a target resource.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Results
                  - Aggregated
                  - By
                  - Target
                  - Resources
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
            /cis/scan/list:
              POST:
                summary: ListCisScans
                description: <p>Returns a CIS scan list.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
            /coverage/list:
              POST:
                summary: ListCoverage
                description: <p>Lists coverage details for you environment.</p>
                tags:
                  - Lists
                  - Coverage
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
            /coverage/statistics/list:
              POST:
                summary: ListCoverageStatistics
                description: >-
                  <p>Lists Amazon Inspector coverage statistics for your
                  environment.</p>
                tags:
                  - Lists
                  - Coverage
                  - Statistics
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
            /delegatedadminaccounts/list:
              POST:
                summary: ListDelegatedAdminAccounts
                description: >-
                  <p>Lists information about the Amazon Inspector delegated
                  administrator of your organization.</p>
                tags:
                  - Lists
                  - Delegated
                  - Administrative
                  - Accounts
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
            /filters/list:
              POST:
                summary: ListFilters
                description: <p>Lists the filters associated with your account.</p>
                tags:
                  - Lists
                  - Filters
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
            /findings/aggregation/list:
              POST:
                summary: ListFindingAggregations
                description: >-
                  <p>Lists aggregated finding data for your environment based on
                  specific criteria.</p>
                tags:
                  - Lists
                  - Findings
                  - Aggregations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
            /findings/list:
              POST:
                summary: ListFindings
                description: <p>Lists findings for your environment.</p>
                tags:
                  - Lists
                  - Findings
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
            /members/list:
              POST:
                summary: ListMembers
                description: >-
                  <p>List members associated with the Amazon Inspector delegated
                  administrator for your organization.</p>
                tags:
                  - Lists
                  - Members
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
            /usage/list:
              POST:
                summary: ListUsageTotals
                description: >-
                  <p>Lists the Amazon Inspector usage totals over the last 30
                  days.</p>
                tags:
                  - Lists
                  - Usage
                  - Totals
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
            /encryptionkey/reset:
              PUT:
                summary: ResetEncryptionKey
                description: >-
                  <p>Resets an encryption key. After the key is reset your
                  resources will be encrypted by an Amazon Web Services owned
                  key.</p>
                tags:
                  - Reset
                  - Encryption
                  - Keys
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
            /vulnerabilities/search:
              POST:
                summary: SearchVulnerabilities
                description: >-
                  <p>Lists Amazon Inspector coverage details for a specific
                  vulnerability.</p>
                tags:
                  - Search
                  - Vulnerabilities
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
            /cissession/health/send:
              PUT:
                summary: SendCisSessionHealth
                description: >-
                  <p> Sends a CIS session health. This API is used by the Amazon
                  Inspector SSM plugin to communicate with the Amazon Inspector
                  service. The Amazon Inspector SSM plugin calls this API to
                  start a CIS scan session for the scan ID supplied by the
                  service. </p>
                tags:
                  - Send
                  - ~~
                  - Sessions
                  - Health
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
            /cissession/telemetry/send:
              PUT:
                summary: SendCisSessionTelemetry
                description: >-
                  <p> Sends a CIS session telemetry. This API is used by the
                  Amazon Inspector SSM plugin to communicate with the Amazon
                  Inspector service. The Amazon Inspector SSM plugin calls this
                  API to start a CIS scan session for the scan ID supplied by
                  the service. </p>
                tags:
                  - Send
                  - ~~
                  - Sessions
                  - Telemetry
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
            /cissession/start:
              PUT:
                summary: StartCisSession
                description: >-
                  <p> Starts a CIS session. This API is used by the Amazon
                  Inspector SSM plugin to communicate with the Amazon Inspector
                  service. The Amazon Inspector SSM plugin calls this API to
                  start a CIS scan session for the scan ID supplied by the
                  service. </p>
                tags:
                  - Start
                  - ~~
                  - Sessions
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
            /cissession/stop:
              PUT:
                summary: StopCisSession
                description: >-
                  <p> Stops a CIS session. This API is used by the Amazon
                  Inspector SSM plugin to communicate with the Amazon Inspector
                  service. The Amazon Inspector SSM plugin calls this API to
                  start a CIS scan session for the scan ID supplied by the
                  service. </p>
                tags:
                  - Stop
                  - ~~
                  - Sessions
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /cis/scan-configuration/update:
              POST:
                summary: UpdateCisScanConfiguration
                description: <p>Updates a CIS scan configuration.</p>
                tags:
                  - Update
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /configuration/update:
              POST:
                summary: UpdateConfiguration
                description: >-
                  <p>Updates setting configurations for your Amazon Inspector
                  account. When you use this API as an Amazon Inspector
                  delegated administrator this updates the setting for all
                  accounts you manage. Member accounts in an organization cannot
                  update this setting.</p>
                tags:
                  - Update
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /ec2deepinspectionconfiguration/update:
              POST:
                summary: UpdateEc2DeepInspectionConfiguration
                description: >-
                  <p>Activates, deactivates Amazon Inspector deep inspection, or
                  updates custom paths for your account. </p>
                tags:
                  - Update
                  - EC2
                  - Deep
                  - Inspections
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /encryptionkey/update:
              PUT:
                summary: UpdateEncryptionKey
                description: >-
                  <p>Updates an encryption key. A
                  <code>ResourceNotFoundException</code> means that an Amazon
                  Web Services owned key is being used for encryption.</p>
                tags:
                  - Update
                  - Encryption
                  - Keys
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /filters/update:
              POST:
                summary: UpdateFilter
                description: >-
                  <p>Specifies the action that is to be applied to the findings
                  that match the filter.</p>
                tags:
                  - Update
                  - Filter
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /ec2deepinspectionconfiguration/org/update:
              POST:
                summary: UpdateOrgEc2DeepInspectionConfiguration
                description: >-
                  <p>Updates the Amazon Inspector deep inspection custom paths
                  for your organization. You must be an Amazon Inspector
                  delegated administrator to use this API.</p>
                tags:
                  - Update
                  - Organizations
                  - EC2
                  - Deep
                  - Inspections
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
                  - Organizations
            /organizationconfiguration/update:
              POST:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the configurations for your Amazon Inspector
                  organiz
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
                  - O
    overlays:
      - type: APIs.io Search
        url: overlays/inspector2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/inspector2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:inspector2
  - name: macie2
    description: >-
      <p>Amazon Macie is a fully managed data security and data privacy service
      that uses machine learning and pattern matching to help you discover and
      protect your sensitive data in AWS. Macie automates the discovery of
      sensitive data, such as PII and intellectual property, to provide you with
      insight into the data that your organization stores in AWS. Macie also
      provides an inventory of your Amazon S3 buckets, which it continually
      monitors for you. If Macie detects sensitive data or potential data access
      issues, it generates detailed findings for you to review and act upon as
      necessary.</p>
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
            title: macie2
          paths:
            /invitations/accept:
              POST:
                summary: AcceptInvitation
                description: >-
                  <p>Accepts an Amazon Macie membership invitation that was
                  received from a specific account.</p>
                tags:
                  - Accept
                  - Invitation
                  - Invitations
                  - Accept
            /custom-data-identifiers/get:
              POST:
                summary: BatchGetCustomDataIdentifiers
                description: >-
                  <p>Retrieves information about one or more custom data
                  identifiers.</p>
                tags:
                  - Batches
                  - Get
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
            /allow-lists:
              GET:
                summary: ListAllowLists
                description: >-
                  <p>Retrieves a subset of information about all the allow lists
                  for an account.</p>
                tags:
                  - Lists
                  - Allow
                  - Lists
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
            /jobs:
              POST:
                summary: CreateClassificationJob
                description: >-
                  <p>Creates and defines the settings for a classification
                  job.</p>
                tags:
                  - Create
                  - Classifications
                  - Jobs
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
            /custom-data-identifiers:
              POST:
                summary: CreateCustomDataIdentifier
                description: >-
                  <p>Creates and defines the criteria and other settings for a
                  custom data identifier.</p>
                tags:
                  - Create
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
            /findingsfilters:
              GET:
                summary: ListFindingsFilters
                description: >-
                  <p>Retrieves a subset of information about all the findings
                  filters for an account.</p>
                tags:
                  - Lists
                  - Findings
                  - Filters
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
            /invitations:
              GET:
                summary: ListInvitations
                description: >-
                  <p>Retrieves information about the Amazon Macie membership
                  invitations that were received by an account.</p>
                tags:
                  - Lists
                  - Invitations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
            /members:
              GET:
                summary: ListMembers
                description: >-
                  <p>Retrieves information about the accounts that are
                  associated with an Amazon Macie administrator account.</p>
                tags:
                  - Lists
                  - Members
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
            /findings/sample:
              POST:
                summary: CreateSampleFindings
                description: <p>Creates sample findings.</p>
                tags:
                  - Create
                  - Samples
                  - Findings
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
            /invitations/decline:
              POST:
                summary: DeclineInvitations
                description: >-
                  <p>Declines Amazon Macie membership invitations that were
                  received from specific accounts.</p>
                tags:
                  - Decline
                  - Invitations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
            /allow-lists/{id}:
              PUT:
                summary: UpdateAllowList
                description: <p>Updates the settings for an allow list.</p>
                tags:
                  - Update
                  - Allow
                  - Lists
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
            /custom-data-identifiers/{id}:
              GET:
                summary: GetCustomDataIdentifier
                description: >-
                  <p>Retrieves the criteria and other settings for a custom data
                  identifier.</p>
                tags:
                  - Get
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
            /findingsfilters/{id}:
              PATCH:
                summary: UpdateFindingsFilter
                description: >-
                  <p>Updates the criteria and other settings for a findings
                  filter.</p>
                tags:
                  - Update
                  - Findings
                  - Filter
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
            /invitations/delete:
              POST:
                summary: DeleteInvitations
                description: >-
                  <p>Deletes Amazon Macie membership invitations that were
                  received from specific accounts.</p>
                tags:
                  - Delete
                  - Invitations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
            /members/{id}:
              GET:
                summary: GetMember
                description: >-
                  <p>Retrieves information about an account that's associated
                  with an Amazon Macie administrator account.</p>
                tags:
                  - Get
                  - Members
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
            /datasources/s3:
              POST:
                summary: DescribeBuckets
                description: >-
                  <p>Retrieves (queries) statistical data and other information
                  about one or more S3 buckets that Amazon Macie monitors and
                  analyzes for an account.</p>
                tags:
                  - Describe
                  - Buckets
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
            /jobs/{jobId}:
              PATCH:
                summary: UpdateClassificationJob
                description: <p>Changes the status of a classification job.</p>
                tags:
                  - Update
                  - Classifications
                  - Jobs
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
            /admin/configuration:
              PATCH:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the Amazon Macie configuration settings for an
                  organization in Organizations.</p>
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
            /macie:
              PATCH:
                summary: UpdateMacieSession
                description: >-
                  <p>Suspends or re-enables Amazon Macie, or updates the
                  configuration settings for a Macie account.</p>
                tags:
                  - Update
                  - Macie
                  - Sessions
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
            /admin:
              GET:
                summary: ListOrganizationAdminAccounts
                description: >-
                  <p>Retrieves information about the delegated Amazon Macie
                  administrator account for an organization in
                  Organizations.</p>
                tags:
                  - Lists
                  - Organizations
                  - Administrative
                  - Accounts
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
            /administrator/disassociate:
              POST:
                summary: DisassociateFromAdministratorAccount
                description: >-
                  <p>Disassociates a member account from its Amazon Macie
                  administrator account.</p>
                tags:
                  - Disassociate
                  - From
                  - Administrator
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
            /master/disassociate:
              POST:
                summary: DisassociateFromMasterAccount
                description: >-
                  <p>(Deprecated) Disassociates a member account from its Amazon
                  Macie administrator account. This operation has been replaced
                  by the <link 
                  linkend="DisassociateFromAdministratorAccount">DisassociateFromAdministratorAccount</link>
                  operation.</p>
                tags:
                  - Disassociate
                  - From
                  - Master
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
            /members/disassociate/{id}:
              POST:
                summary: DisassociateMember
                description: >-
                  <p>Disassociates an Amazon Macie administrator account from a
                  member account.</p>
                tags:
                  - Disassociate
                  - Members
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
            /administrator:
              GET:
                summary: GetAdministratorAccount
                description: >-
                  <p>Retrieves information about the Amazon Macie administrator
                  account for an account.</p>
                tags:
                  - Get
                  - Administrator
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
            /automated-discovery/configuration:
              PUT:
                summary: UpdateAutomatedDiscoveryConfiguration
                description: >-
                  <p>Enables or disables automated sensitive data discovery for
                  an account.</p>
                tags:
                  - Update
                  - Automated
                  - Discovery
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
            /datasources/s3/statistics:
              POST:
                summary: GetBucketStatistics
                description: >-
                  <p>Retrieves (queries) aggregated statistical data about all
                  the S3 buckets that Amazon Macie monitors and analyzes for an
                  account.</p>
                tags:
                  - Get
                  - Bucket
                  - Statistics
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
            /classification-export-configuration:
              PUT:
                summary: PutClassificationExportConfiguration
                description: >-
                  <p>Creates or updates the configuration settings for storing
                  data classification results.</p>
                tags:
                  - Put
                  - Classifications
                  - Export
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
            /classification-scopes/{id}:
              PATCH:
                summary: UpdateClassificationScope
                description: >-
                  <p>Updates the classification scope settings for an
                  account.</p>
                tags:
                  - Update
                  - Classifications
                  - Scopes
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
            /findings/statistics:
              POST:
                summary: GetFindingStatistics
                description: >-
                  <p>Retrieves (queries) aggregated statistical data about
                  findings.</p>
                tags:
                  - Get
                  - Findings
                  - Statistics
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
            /findings/describe:
              POST:
                summary: GetFindings
                description: <p>Retrieves the details of one or more findings.</p>
                tags:
                  - Get
                  - Findings
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
            /findings-publication-configuration:
              PUT:
                summary: PutFindingsPublicationConfiguration
                description: >-
                  <p>Updates the configuration settings for publishing findings
                  to Security Hub.</p>
                tags:
                  - Put
                  - Findings
                  - Publication
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
            /invitations/count:
              GET:
                summary: GetInvitationsCount
                description: >-
                  <p>Retrieves the count of Amazon Macie membership invitations
                  that were received by an account.</p>
                tags:
                  - Get
                  - Invitations
                  - Count
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
            /master:
              GET:
                summary: GetMasterAccount
                description: >-
                  <p>(Deprecated) Retrieves information about the Amazon Macie
                  administrator account for an account. This operation has been
                  replaced by the <link 
                  linkend="GetAdministratorAccount">GetAdministratorAccount</link>
                  operation.</p>
                tags:
                  - Get
                  - Master
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
            /resource-profiles:
              PATCH:
                summary: UpdateResourceProfile
                description: <p>Updates the sensitivity score for an S3 bucket.</p>
                tags:
                  - Update
                  - Resources
                  - Profiles
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
            /reveal-configuration:
              PUT:
                summary: UpdateRevealConfiguration
                description: >-
                  <p>Updates the status and configuration settings for
                  retrieving occurrences of sensitive data reported by
                  findings.</p>
                tags:
                  - Update
                  - Reveal
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
            /findings/{findingId}/reveal:
              GET:
                summary: GetSensitiveDataOccurrences
                description: >-
                  <p>Retrieves occurrences of sensitive data reported by a
                  finding.</p>
                tags:
                  - Get
                  - Sensitive
                  - Data
                  - Occurrences
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
            /findings/{findingId}/reveal/availability:
              GET:
                summary: GetSensitiveDataOccurrencesAvailability
                description: >-
                  <p>Checks whether occurrences of sensitive data can be
                  retrieved for a finding.</p>
                tags:
                  - Get
                  - Sensitive
                  - Data
                  - Occurrences
                  - Availability
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
            /templates/sensitivity-inspections/{id}:
              PUT:
                summary: UpdateSensitivityInspectionTemplate
                description: ' <p>Updates the settings for the sensitivity inspection template for an account.</p>'
                tags:
                  - Update
                  - Sensitivity
                  - Inspections
                  - Templates
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
            /usage/statistics:
              POST:
                summary: GetUsageStatistics
                description: >-
                  <p>Retrieves (queries) quotas and aggregated usage data for
                  one or more accounts.</p>
                tags:
                  - Get
                  - Usage
                  - Statistics
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
            /usage:
              GET:
                summary: GetUsageTotals
                description: >-
                  <p>Retrieves (queries) aggregated usage data for an
                  account.</p>
                tags:
                  - Get
                  - Usage
                  - Totals
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
            /jobs/list:
              POST:
                summary: ListClassificationJobs
                description: >-
                  <p>Retrieves a subset of information about one or more
                  classification jobs.</p>
                tags:
                  - Lists
                  - Classifications
                  - Jobs
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /classification-scopes:
              GET:
                summary: ListClassificationScopes
                description: >-
                  <p>Retrieves a subset of information about the classification
                  scope for an account.</p>
                tags:
                  - Lists
                  - Classifications
                  - Scopes
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /custom-data-identifiers/list:
              POST:
                summary: ListCustomDataIdentifiers
                description: >-
                  <p>Retrieves a subset of information about all the custom data
                  identifiers for an account.</p>
                tags:
                  - Lists
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /findings:
              POST:
                summary: ListFindings
                description: >-
                  <p>Retrieves a subset of information about one or more
                  findings.</p>
                tags:
                  - Lists
                  - Findings
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /managed-data-identifiers/list:
              POST:
                summary: ListManagedDataIdentifiers
                description: >-
                  <p>Retrieves information about all the managed data
                  identifiers that Amazon Macie currently provides.</p>
                tags:
                  - Lists
                  - Managed
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
            /resource-profiles/artifacts:
              GET:
                summary: ListResourceProfileArtifacts
                description: >-
                  <p>Retrieves information about objects that were selected from
                  an S3 bucket for automated sensitive data discovery.</p>
                tags:
                  - Lists
                  - Resources
                  - Profiles
                  - Artifacts
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
            /resource-profiles/detections:
              PATCH:
                summary: UpdateResourceProfileDetections
                description: >-
                  <p>Updates the sensitivity scoring settings for an S3
                  bucket.</p>
                tags:
                  - Update
                  - Resources
                  - Profiles
                  - Detections
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
            /templates/sensitivity-inspections:
              GET:
                summary: ListSensitivityInspectionTemplates
                description: ' <p>Retrieves a subset of information about the sensitivity inspection template for an account.</p>'
                tags:
                  - Lists
                  - Sensitivity
                  - Inspections
                  - Templates
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags (keys and values) from an Amazon
                  Macie resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
            /datasources/search-resources:
              POST:
                summary: SearchResources
                description: >-
                  <p>Retrieves (queries) statistical data and other information
                  about Amazon Web Services resources that Amazon Macie monitors
                  and analyzes.</p>
                tags:
                  - Search
                  - Resources
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
                  - Search
                  - Resources
            /custom-data-identifiers/test:
              POST:
                summary: TestCustomDataIdentifier
                description: <p>Tests a custom data identifier.</p>
                tags:
                  - Tests
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
                  - Search
                  - Resources
                  - Tests
            /macie/members/{id}:
              PATCH:
                summary: UpdateMemberSession
                description: >-
                  <p>Enables an Amazon Macie administrator to suspend or
                  re-enable Macie for a member ac
                tags:
                  - Update
                  - Members
                  - Sessions
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
                  - Search
                  - Resources
                  - Te
    overlays:
      - type: APIs.io Search
        url: overlays/macie2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/macie2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:macie2
  - name: repostspace
    description: >-
      <p>AWS re:Post Private is a private version of AWS re:Post for enterprises
      with Enterprise Support or Enterprise On-Ramp Support plans. It provides
      access to knowledge and experts to accelerate cloud adoption and increase
      developer productivity. With your organization-specific private re:Post,
      you can build an organization-specific developer community that drives
      efficiencies at scale and provides access to valuable knowledge resources.
      Additionally, re:Post Private centralizes trusted AWS technical content
      and offers private discussion forums to improve how your teams collaborate
      internally and with AWS to remove technical obstacles, accelerate
      innovation, and scale more efficiently in the cloud.</p>
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
            title: repostspace
          paths:
            /spaces:
              GET:
                summary: ListSpaces
                description: >-
                  <p>Returns a list of AWS re:Post Private private re:Posts in
                  the account with some information about each private
                  re:Post.</p>
                tags:
                  - Lists
                  - Spaces
                  - Spaces
            /spaces/{spaceId}:
              PUT:
                summary: UpdateSpace
                description: >-
                  <p>Modifies an existing AWS re:Post Private private
                  re:Post.</p>
                tags:
                  - Update
                  - Space
                  - Spaces
                  - Identifiers
            /spaces/{spaceId}/admins/{adminId}:
              POST:
                summary: RegisterAdmin
                description: >-
                  <p>Adds a user or group to the list of administrators of the
                  private re:Post.</p>
                tags:
                  - Register
                  - Administrative
                  - Spaces
                  - Identifiers
                  - Administrator
                  - Administrative
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes the association of the tag with the AWS re:Post
                  Private resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Spaces
                  - Identifiers
                  - Administrator
                  - Administrative
                  - ARN
            /spaces/{spaceId}/invite:
              POST:
                summary: SendInvites
                description: <p>Sends an invitation email to selected users and g
                tags:
                  - Send
                  - Invites
                  - Spaces
                  - Identifiers
                  - Administrator
                  - Administrative
                  - ARN
                  - Invi
    overlays:
      - type: APIs.io Search
        url: overlays/repostspace-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/repostspace-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:repostspace
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
  - name: GitLab REST API
    description: >+
      The REST APIs have been around for a longer time compared to GraphQL APIs,
      which may make them more familiar to some developers. It is often a good
      choice for developers who are more comfortable with traditional API
      architecture.

    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.gitlab.com/ee/api/rest/index.html
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.gitlab.com/ee/api/rest/index.html
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: GitLab API
            license:
              name: CC BY-SA 4.0
              url: https://gitlab.com/gitlab-org/gitlab/-/blob/master/LICENSE
          tags:
            - name: badges
              description: Operations about badges
            - name: branches
              description: Operations about branches
            - name: alert_management
              description: Operations about alert_managements
            - name: batched_background_migrations
              description: Operations about batched_background_migrations
            - name: admin
              description: Operations about admins
            - name: migrations
              description: Operations about migrations
            - name: applications
              description: Operations about applications
            - name: avatar
              description: Operations about avatars
            - name: broadcast_messages
              description: Operations about broadcast_messages
            - name: bulk_imports
              description: Operations about bulk_imports
            - name: application
              description: Operations about applications
            - name: access_requests
              description: Operations related to access requests
            - name: ci_lint
              description: Operations related to linting a CI config file
            - name: ci_resource_groups
              description: Operations to manage job concurrency with resource groups
            - name: ci_variables
              description: Operations related to CI/CD variables
            - name: cluster_agents
              description: Operations related to the GitLab agent for Kubernetes
            - name: clusters
              description: Operations related to clusters
            - name: composer_packages
              description: Operations related to Composer packages
            - name: conan_packages
              description: Operations related to Conan packages
            - name: container_registry
              description: Operations related to container registry
            - name: container_registry_event
              description: Operations related to container registry events
            - name: dashboard_annotations
              description: Operations related to dashboard annotations
            - name: debian_distribution
              description: Operations related to Debian Linux distributions
            - name: debian_packages
              description: Operations related to Debian Linux packages
            - name: dependency_proxy
              description: Operations to manage dependency proxy for a groups
            - name: deploy_keys
              description: Operations related to deploy keys
            - name: deploy_tokens
              description: Operations related to deploy tokens
            - name: deployments
              description: Operations related to deployments
            - name: dora_metrics
              description: >-
                Operations related to DevOps Research and Assessment (DORA) key
                metrics
            - name: environments
              description: Operations related to environments
            - name: error_tracking_client_keys
              description: Operations related to error tracking client keys
            - name: error_tracking_project_settings
              description: Operations related to error tracking project settings
            - name: feature_flags_user_lists
              description: Operations related to accessing GitLab feature flag user lists
            - name: feature_flags
              description: Operations related to feature flags
            - name: features
              description: Operations related to managing Flipper-based feature flags
            - name: freeze_periods
              description: Operations related to deploy freeze periods
            - name: generic_packages
              description: Operations related to Generic packages
            - name: geo
              description: Operations related to Geo
            - name: geo_nodes
              description: Operations related Geo Nodes
            - name: go_proxy
              description: Operations related to Go Proxy
            - name: group_export
              description: Operations related to exporting groups
            - name: group_import
              description: Operations related to importing groups
            - name: group_packages
              description: Operations related to group packages
            - name: helm_packages
              description: Operations related to Helm packages
            - name: integrations
              description: Operations related to integrations
            - name: issue_links
              description: Operations related to issue links
            - name: jira_connect_subscriptions
              description: Operations related to JiraConnect subscriptions
            - name: jobs
              description: Operations related to CI Jobs
            - name: maven_packages
              description: Operations related to Maven packages
            - name: merge_requests
              description: Operations related to merge requests
            - name: metadata
              description: Operations related to metadata of the GitLab instance
            - name: metrics_user_starred_dashboards
              description: Operations related to User-starred metrics dashboards
            - name: ml_model_registry
              description: Operations related to Model registry
            - name: npm_packages
              description: Operations related to NPM packages
            - name: nuget_packages
              description: Operations related to Nuget packages
            - name: package_files
              description: Operations about package files
            - name: plan_limits
              description: Operations related to plan limits
            - name: project_export
              description: Operations related to exporting projects
            - name: project_hooks
              description: Operations related to project hooks
            - name: project_import
              description: Operations related to importing projects
            - name: project_import_bitbucket
              description: Operations related to importing BitBucket projects
            - name: project_import_github
              description: Operations related to importing GitHub projects
            - name: project_packages
              description: Operations related to project packages
            - name: projects
              description: Operations related to projects
            - name: protected environments
              description: Operations related to protected environments
            - name: pypi_packages
              description: Operations related to PyPI packages
            - name: release_links
              description: Operations related to release assets (links)
            - name: releases
              description: Operations related to releases
            - name: resource_milestone_events
              description: Operations about resource milestone events
            - name: rpm_packages
              description: Operations related to RPM packages
            - name: rubygem_packages
              description: Operations related to RubyGems
            - name: suggestions
              description: Operations related to suggestions
            - name: system_hooks
              description: Operations related to system hooks
            - name: terraform_state
              description: Operations related to Terraform state files
            - name: terraform_registry
              description: Operations related to the Terraform module registry
            - name: unleash_api
              description: Operations related to Unleash API
          paths:
            /api/v4/groups/{id}/badges/{badge_id}:
              get:
                tags:
                  - Gets
                  - Badge
                  - Of
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Gets a badge of a group.
                description: This feature was introduced in GitLab 10.6.
              put:
                tags:
                  - Updates
                  - Badge
                  - Of
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Updates a badge of a group.
                description: This feature was introduced in GitLab 10.6.
              delete:
                tags:
                  - Removes
                  - Badge
                  - From
                  - The
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Removes a badge from the group.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/groups/{id}/badges:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Group
                  - Badges
                  - Viewable
                  - By
                  - The
                  - Authenticated
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: >-
                  Gets a list of group badges viewable by the authenticated
                  user.
                description: This feature was introduced in GitLab 10.6.
              post:
                tags:
                  - Adds
                  - Badge
                  - To
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Adds a badge to a group.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/groups/{id}/badges/render:
              get:
                tags:
                  - Preview
                  - Badge
                  - From
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                summary: Preview a badge from a group.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/groups/{id}/access_requests/{user_id}:
              delete:
                tags:
                  - Denies
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                summary: Denies an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/groups/{id}/access_requests/{user_id}/approve:
              put:
                tags:
                  - Approves
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                summary: Approves an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/groups/{id}/access_requests:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Access
                  - Requests
                  - For
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                summary: Gets a list of access requests for a group.
                description: This feature was introduced in GitLab 8.11.
              post:
                tags:
                  - Requests
                  - Access
                  - For
                  - The
                  - Authenticated
                  - User
                  - To
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                summary: Requests access for the authenticated user to a group.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/repository/merged_branches:
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                description: Delete all merged branches
            /api/v4/projects/{id}/repository/branches/{branch}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Get a single repository branch
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Delete a branch
              head:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Check if a branch exists
            /api/v4/projects/{id}/repository/branches:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Get a project repository branches
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Create branch
            /api/v4/projects/{id}/repository/branches/{branch}/unprotect:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                description: Unprotect a single branch
            /api/v4/projects/{id}/repository/branches/{branch}/protect:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                description: Protect a single branch
            /api/v4/projects/{id}/badges/{badge_id}:
              get:
                tags:
                  - Gets
                  - Badge
                  - Of
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Gets a badge of a project.
                description: This feature was introduced in GitLab 10.6.
              put:
                tags:
                  - Updates
                  - Badge
                  - Of
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Updates a badge of a project.
                description: This feature was introduced in GitLab 10.6.
              delete:
                tags:
                  - Removes
                  - Badge
                  - From
                  - The
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Removes a badge from the project.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/projects/{id}/badges:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Project
                  - Badges
                  - Viewable
                  - By
                  - The
                  - Authenticated
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: >-
                  Gets a list of project badges viewable by the authenticated
                  user.
                description: This feature was introduced in GitLab 10.6.
              post:
                tags:
                  - Adds
                  - Badge
                  - To
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Adds a badge to a project.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/projects/{id}/badges/render:
              get:
                tags:
                  - Preview
                  - Badge
                  - From
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Preview a badge from a project.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/projects/{id}/access_requests/{user_id}:
              delete:
                tags:
                  - Denies
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Denies an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/access_requests/{user_id}/approve:
              put:
                tags:
                  - Approves
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Approves an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/access_requests:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Access
                  - Requests
                  - For
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Gets a list of access requests for a project.
                description: This feature was introduced in GitLab 8.11.
              post:
                tags:
                  - Requests
                  - Access
                  - For
                  - The
                  - Authenticated
                  - User
                  - To
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Requests access for the authenticated user to a project.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/alert_management_alerts/{alert_iid}/metric_images/{metric_image_id}:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Update a metric image for an alert
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Remove a metric image for an alert
            /api/v4/projects/{id}/alert_management_alerts/{alert_iid}/metric_images:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Metric Images for alert
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Upload a metric image for an alert
            /api/v4/projects/{id}/alert_management_alerts/{alert_iid}/metric_images/authorize:
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                description: Workhorse authorize metric image file upload
            /api/v4/admin/batched_background_migrations/{id}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                description: Retrieve a batched background migration
            /api/v4/admin/batched_background_migrations:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                description: Get the list of batched background migrations
            /api/v4/admin/batched_background_migrations/{id}/resume:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                description: Resume a batched background migration
            /api/v4/admin/batched_background_migrations/{id}/pause:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                description: Pause a batched background migration
            /api/v4/admin/ci/variables/{key}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Get the details of a specific instance-level variable
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Update an instance-level variable
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Delete an existing instance-level variable
            /api/v4/admin/ci/variables:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: List all instance-level variables
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Create a new instance-level variable
            /api/v4/admin/databases/{database_name}/dictionary/tables/{table_name}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                description: Retrieve dictionary details
            /api/v4/admin/clusters/{cluster_id}:
              get:
                tags:
                  - Get
                  - Single
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                summary: Get a single instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Returns a single
                  instance cluster.
              put:
                tags:
                  - Edit
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                summary: Edit instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Updates an
                  existing instance cluster.
              delete:
                tags:
                  - Delete
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                summary: Delete instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Deletes an
                  existing instance cluster. Does not remove existing resources
                  within the connected Kubernetes cluster.
            /api/v4/admin/clusters/add:
              post:
                tags:
                  - Add
                  - Existing
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                summary: Add existing instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Adds an existing
                  Kubernetes instance cluster.
            /api/v4/admin/clusters:
              get:
                tags:
                  - List
                  - Instance
                  - Clusters
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                summary: List instance clusters
                description: >-
                  This feature was introduced in GitLab 13.2. Returns a list of
                  instance clusters.
            /api/v4/admin/migrations/{timestamp}/mark:
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                description: Mark the migration as successfully executed
            /api/v4/applications/{id}:
              delete:
                tags:
                  - Delete
                  - An
                  - Application
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                summary: Delete an application
                description: Delete a specific application
            /api/v4/applications:
              get:
                tags:
                  - Get
                  - Applications
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                summary: Get applications
                description: List all registered applications
              post:
                tags:
                  - Create
                  - New
                  - Application
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                summary: Create a new application
                description: This feature was introduced in GitLab 10.5
            /api/v4/avatar:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                description: Return avatar url for a user
            /api/v4/broadcast_messages/{id}:
              get:
                tags:
                  - Get
                  - Specific
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Get a specific broadcast message
                description: This feature was introduced in GitLab 8.12.
              put:
                tags:
                  - Update
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Update a broadcast message
                description: This feature was introduced in GitLab 8.12.
              delete:
                tags:
                  - Delete
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Delete a broadcast message
                description: This feature was introduced in GitLab 8.12.
            /api/v4/broadcast_messages:
              get:
                tags:
                  - Get
                  - All
                  - Broadcast
                  - Messages
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Get all broadcast messages
                description: This feature was introduced in GitLab 8.12.
              post:
                tags:
                  - Create
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Create a broadcast message
                description: This feature was introduced in GitLab 8.12.
            /api/v4/bulk_imports/{import_id}/entities/{entity_id}:
              get:
                tags:
                  - Get
                  - Git
                  - Lab
                  - Migration
                  - Entity
                  - Details
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: Get GitLab Migration entity details
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports/{import_id}/entities:
              get:
                tags:
                  - List
                  - Git
                  - Lab
                  - Migration
                  - Entities
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: List GitLab Migration entities
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports/{import_id}:
              get:
                tags:
                  - Get
                  - Git
                  - Lab
                  - Migration
                  - Details
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: Get GitLab Migration details
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports/entities:
              get:
                tags:
                  - List
                  - All
                  - Git
                  - Lab
                  - Migrations'
                  - Entities
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: List all GitLab Migrations' entities
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports:
              get:
                tags:
                  - List
                  - All
                  - Git
                  - Lab
                  - Migrations
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: List all GitLab Migrations
                description: This feature was introduced in GitLab 14.1.
              post:
                tags:
                  - Start
                  - New
                  - Git
                  - Lab
                  - Migration
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: Start a new GitLab Migration
                description: This feature was introduced in GitLab 14.2.
            /api/v4/application/appearance:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                description: Get the current appearance
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                description: Modify appearance
            /api/v4/application/plan_limits:
              get:
                tags:
                  - Get
                  - Current
                  - Plan
                  - Limits
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                summary: Get current plan limits
                description: List the current limits of a plan on the GitLab instance.
              put:
                tags:
                  - Change
                  - Plan
                  - Limits
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                summary: Change plan limits
                description: Modify the limits of a plan on the GitLab instance.
            /api/v4/metadata:
              get:
                tags:
                  - Retrieve
                  - Metadata
                  - Information
                  - For
                  - This
                  - Git
                  - Lab
                  - Instance
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                summary: Retrieve metadata information for this GitLab instance
                description: This feature was introduced in GitLab 15.2.
            /api/v4/version:
              get:
                tags:
                  - Retrieves
                  - Version
                  - Information
                  - For
                  - The
                  - Git
                  - Lab
                  - Instance
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                summary: Retrieves version information for the GitLab instance
                description: >-
                  This feature was introduced in GitLab 8.13 and deprecated in
                  15.5. We recommend you instead use the Metadata API.
            /api/v4/projects/{id}/jobs:
              get:
                tags:
                  - List
                  - Jobs
                  - For
                  - Project
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                  - Jobs
                summary: List jobs for a project
            /api/v4/projects/{id}/jobs/{job_id}:
              get:
                tags:
                  - Get
                  - Single
                  - Job
                  - By
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                  - Jobs
                  - Job_id
                summary: Get a single job by ID
            /api/v4/projects/{id}/jobs/{job_id}/play:
              post:
                tags:
                  - Run
                  - Ma
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                  - Jobs
                  - Job_id
                  - Play
                summary: Run a
      - type: Authentication
        url: https://docs.gitlab.com/ee/api/rest/index.html#authentication
      - type: Status Codes
        url: https://docs.gitlab.com/ee/api/rest/index.html#status-codes
      - type: SDKs
        url: https://docs.gitlab.com/ee/api/rest/index.html#third-party-clients
      - type: Rate Limits
        url: https://docs.gitlab.com/ee/api/rest/index.html#rate-limits
    overlays:
      - type: APIs.io Search
        url: overlays/gitlab-openapi-original.yml
      - type: API Evangelist Ratings
        url: overlays/gitlab-openapi-api-evangelist-ratings.yaml
      - type: APIs.io Search
        url: overlays/gitlab-openapi-search.yml
    aid: gitlab:gitlab-rest-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---