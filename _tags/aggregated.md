---
name: Aggregated
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/aggregated.png
url: https://example.com/apis/aggregated.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Aggregated
apis:
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
  - name: models.lex.v2
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
            title: models.lex.v2
          paths:
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchcreate:
              PUT:
                summary: BatchCreateCustomVocabularyItem
                description: >-
                  <p>Create a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Create
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchdelete:
              POST:
                summary: BatchDeleteCustomVocabularyItem
                description: >-
                  <p>Delete a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Delete
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchupdate:
              PUT:
                summary: BatchUpdateCustomVocabularyItem
                description: >-
                  <p>Update a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Update
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/:
              PUT:
                summary: UpdateBotLocale
                description: >-
                  <p>Updates the settings that a bot has for a specific
                  locale.</p>
                tags:
                  - Update
                  - Bot
                  - Locales
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
            /bots/:
              POST:
                summary: ListBots
                description: <p>Gets a list of available bots.</p>
                tags:
                  - Lists
                  - Bots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
            /bots/{botId}/botaliases/:
              POST:
                summary: ListBotAliases
                description: <p>Gets a list of aliases for the specified bot.</p>
                tags:
                  - Lists
                  - Bot
                  - Aliases
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
            /bots/{botId}/botversions/{botVersion}/botlocales/:
              POST:
                summary: ListBotLocales
                description: <p>Gets a list of locales for the specified bot.</p>
                tags:
                  - Lists
                  - Bot
                  - Locales
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
            /bots/{botId}/replicas/:
              POST:
                summary: ListBotReplicas
                description: <p>The action to list the replicated bots.</p>
                tags:
                  - Lists
                  - Bot
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
            /bots/{botId}/botversions/:
              POST:
                summary: ListBotVersions
                description: >-
                  <p>Gets information about all of the versions of a bot.</p>
                  <p>The <code>ListBotVersions</code> operation returns a
                  summary of each version of a bot. For example, if a bot has
                  three numbered versions, the <code>ListBotVersions</code>
                  operation returns for summaries, one for each numbered version
                  and one for the <code>DRAFT</code> version.</p> <p>The
                  <code>ListBotVersions</code> operation always returns at least
                  one version, the <code>DRAFT</code> version.</p>
                tags:
                  - Lists
                  - Bot
                  - Versions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
            /exports/:
              POST:
                summary: ListExports
                description: >-
                  <p>Lists the exports for a bot, bot locale, or custom
                  vocabulary. Exports are kept in the list for 7 days.</p>
                tags:
                  - Lists
                  - Exports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/:
              POST:
                summary: ListIntents
                description: <p>Get a list of intents that meet the specified criteria.</p>
                tags:
                  - Lists
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
            /policy/{resourceArn}/:
              PUT:
                summary: UpdateResourcePolicy
                description: >-
                  <p>Replaces the existing resource policy for a bot or bot
                  alias with a new one. If the policy doesn't exist, Amazon Lex
                  returns an exception.</p>
                tags:
                  - Update
                  - Resources
                  - Policies
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
            /policy/{resourceArn}/statements/:
              POST:
                summary: CreateResourcePolicyStatement
                description: >-
                  <p>Adds a new resource policy statement to a bot or bot alias.
                  If a resource policy exists, the statement is added to the
                  current resource policy. If a policy doesn't exist, a new
                  policy is created.</p> <p>You can't create a resource policy
                  statement that allows cross-account access.</p>
                tags:
                  - Create
                  - Resources
                  - Policies
                  - Statements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/slots/:
              POST:
                summary: ListSlots
                description: <p>Gets a list of slots that match the specified criteria.</p>
                tags:
                  - Lists
                  - Slots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/slottypes/:
              POST:
                summary: ListSlotTypes
                description: >-
                  <p>Gets a list of slot types that match the specified
                  criteria.</p>
                tags:
                  - Lists
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
            /testsets/{testSetId}/testsetdiscrepancy:
              POST:
                summary: CreateTestSetDiscrepancyReport
                description: >-
                  <p>Create a report that describes the differences between the
                  bot and the test set.</p>
                tags:
                  - Create
                  - Tests
                  - Sets
                  - Discrepancy
                  - Reports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
            /createuploadurl/:
              POST:
                summary: CreateUploadUrl
                description: >-
                  <p>Gets a pre-signed S3 write URL that you use to upload the
                  zip archive when importing a bot or a bot locale. </p>
                tags:
                  - Create
                  - Uploads
                  - URL
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
            /bots/{botId}/:
              PUT:
                summary: UpdateBot
                description: <p>Updates the configuration of an existing bot. </p>
                tags:
                  - Update
                  - Bot
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
            /bots/{botId}/botaliases/{botAliasId}/:
              PUT:
                summary: UpdateBotAlias
                description: <p>Updates the configuration of an existing bot alias.</p>
                tags:
                  - Update
                  - Bot
                  - Alias
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
            /bots/{botId}/replicas/{replicaRegion}/:
              GET:
                summary: DescribeBotReplica
                description: >-
                  <p>Monitors the bot replication status through the UI
                  console.</p>
                tags:
                  - Describe
                  - Bot
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/:
              GET:
                summary: DescribeBotVersion
                description: <p>Provides metadata about a version of a bot.</p>
                tags:
                  - Describe
                  - Bot
                  - Versions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary:
              DELETE:
                summary: DeleteCustomVocabulary
                description: >-
                  <p>Removes a custom vocabulary from the specified locale in
                  the specified bot.</p>
                tags:
                  - Delete
                  - Custom
                  - Vocabularies
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /exports/{exportId}/:
              PUT:
                summary: UpdateExport
                description: >-
                  <p>Updates the password used to protect an export zip
                  archive.</p> <p>The password is not required. If you don't
                  supply a password, Amazon Lex generates a zip file that is not
                  protected by a password. This is the archive that is available
                  at the pre-signed S3 URL provided by the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_DescribeExport.html">DescribeExport</a>
                  operation.</p>
                tags:
                  - Update
                  - Export
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /imports/{importId}/:
              GET:
                summary: DescribeImport
                description: <p>Gets information about a specific import.</p>
                tags:
                  - Describe
                  - Import
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/:
              PUT:
                summary: UpdateIntent
                description: <p>Updates the settings for an intent.</p>
                tags:
                  - Update
                  - Intent
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /policy/{resourceArn}/statements/{statementId}/:
              DELETE:
                summary: DeleteResourcePolicyStatement
                description: >-
                  <p>Deletes a policy statement from a resource policy. If you
                  delete the last statement from a policy, the policy is
                  deleted. If you specify a statement ID that doesn't exist in
                  the policy, or if the bot or bot alias doesn't have a policy
                  attached, Amazon Lex returns an exception.</p>
                tags:
                  - Delete
                  - Resources
                  - Policies
                  - Statements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/slots/{slotId}/:
              PUT:
                summary: UpdateSlot
                description: <p>Updates the settings for a slot.</p>
                tags:
                  - Update
                  - Slots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/slottypes/{slotTypeId}/:
              PUT:
                summary: UpdateSlotType
                description: <p>Updates the configuration of an existing slot type.</p>
                tags:
                  - Update
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
            /testsets/{testSetId}:
              PUT:
                summary: UpdateTestSet
                description: <p>The action to update the test set.</p>
                tags:
                  - Update
                  - Tests
                  - Sets
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
            /bots/{botId}/utterances/:
              DELETE:
                summary: DeleteUtterances
                description: >-
                  <p>Deletes stored utterances.</p> <p>Amazon Lex stores the
                  utterances that users send to your bot. Utterances are stored
                  for 15 days for use with the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, and then stored indefinitely for use in improving
                  the ability of your bot to respond to user input..</p> <p>Use
                  the <code>DeleteUtterances</code> operation to manually delete
                  utterances for a specific session. When you use the
                  <code>DeleteUtterances</code> operation, utterances stored for
                  improving your bot's ability to respond to user input are
                  deleted immediately. Utterances stored for use with the
                  <code>ListAggregatedUtterances</code> operation are deleted
                  after 15 days.</p>
                tags:
                  - Delete
                  - Utterances
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/:
              PUT:
                summary: UpdateBotRecommendation
                description: <p>Updates an existing bot recommendation request.</p>
                tags:
                  - Update
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generations/{generationId}:
              GET:
                summary: DescribeBotResourceGeneration
                description: >-
                  <p>Returns information about a request to generate a bot
                  through natural language description, made through the
                  <code>StartBotResource</code> API. Use the
                  <code>generatedBotLocaleUrl</code> to retrieve the Amazon S3
                  object containing the bot locale configuration. You can then
                  modify and import this configuration.</p>
                tags:
                  - Describe
                  - Bot
                  - Resources
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/metadata:
              GET:
                summary: DescribeCustomVocabularyMetadata
                description: >-
                  <p>Provides metadata information about a custom
                  vocabulary.</p>
                tags:
                  - Describe
                  - Custom
                  - Vocabularies
                  - Metadata
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
            /testexecutions/{testExecutionId}:
              GET:
                summary: DescribeTestExecution
                description: <p>Gets metadata information about the test execution.</p>
                tags:
                  - Describe
                  - Tests
                  - Execution
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
            /testsetdiscrepancy/{testSetDiscrepancyReportId}:
              GET:
                summary: DescribeTestSetDiscrepancyReport
                description: >-
                  <p>Gets metadata information about the test set discrepancy
                  report.</p>
                tags:
                  - Describe
                  - Tests
                  - Sets
                  - Discrepancy
                  - Reports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
            /testsetgenerations/{testSetGenerationId}:
              GET:
                summary: DescribeTestSetGeneration
                description: >-
                  <p>Gets metadata information about the test set
                  generation.</p>
                tags:
                  - Describe
                  - Tests
                  - Sets
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generate:
              POST:
                summary: GenerateBotElement
                description: <p>Generates sample utterances for an intent.</p>
                tags:
                  - Generate
                  - Bot
                  - Elements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
            /testexecutions/{testExecutionId}/artifacturl:
              GET:
                summary: GetTestExecutionArtifactsUrl
                description: >-
                  <p>The pre-signed Amazon S3 URL to download the test execution
                  result artifacts.</p>
                tags:
                  - Get
                  - Tests
                  - Execution
                  - Artifacts
                  - URL
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
            /bots/{botId}/aggregatedutterances/:
              POST:
                summary: ListAggregatedUtterances
                description: >-
                  <p>Provides a list of utterances that users have sent to the
                  bot.</p> <p>Utterances are aggregated by the text of the
                  utterance. For example, all instances where customers used the
                  phrase "I want to order pizza" are aggregated into the same
                  line in the response.</p> <p>You can see both detected
                  utterances and missed utterances. A detected utterance is
                  where the bot properly recognized the utterance and activated
                  the associated intent. A missed utterance was not recognized
                  by the bot and didn't activate an intent.</p> <p>Utterances
                  can be aggregated for a bot alias or for a bot version, but
                  not both at the same time.</p> <p>Utterances statistics are
                  not generated under the following conditions:</p> <ul> <li>
                  <p>The <code>childDirected</code> field was set to true when
                  the bot was created.</p> </li> <li> <p>You are using slot
                  obfuscation with one or more slots.</p> </li> <li> <p>You
                  opted out of participating in improving Amazon Lex.</p> </li>
                  </ul>
                tags:
                  - Lists
                  - Aggregated
                  - Utterances
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/replicas/{replicaRegion}/botaliases/:
              POST:
                summary: ListBotAliasReplicas
                description: >-
                  <p>The action to list the replicated bots created from the
                  source bot alias.</p>
                tags:
                  - Lists
                  - Bot
                  - Alias
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/:
              PUT:
                summary: StartBotRecommendation
                description: >-
                  <p>Use this to provide your transcript data, and to start the
                  bot recommendation process.</p>
                tags:
                  - Start
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generations:
              POST:
                summary: ListBotResourceGenerations
                description: <p>Lists the generation requests made for a bot locale.</p>
                tags:
                  - Lists
                  - Bot
                  - Resources
                  - Generations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/replicas/{replicaRegion}/botversions/:
              POST:
                summary: ListBotVersionReplicas
                description: >-
                  <p>Contains information about all the versions replication
                  statuses applicable for Global Resiliency.</p>
                tags:
                  - Lists
                  - Bot
                  - Versions
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /builtins/locales/{localeId}/intents/:
              POST:
                summary: ListBuiltInIntents
                description: >-
                  <p>Gets a list of built-in intents provided by Amazon Lex that
                  you can use in your bot. </p> <p>To use a built-in intent as a
                  the base for your own intent, include the built-in intent
                  signature in the <code>parentIntentSignature</code> parameter
                  when you call the <code>CreateIntent</code> operation. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_CreateIntent.html">CreateIntent</a>.</p>
                tags:
                  - Lists
                  - Built
                  - In
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /builtins/locales/{localeId}/slottypes/:
              POST:
                summary: ListBuiltInSlotTypes
                description: >-
                  <p>Gets a list of built-in slot types that meet the specified
                  criteria.</p>
                tags:
                  - Lists
                  - Built
                  - In
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/list:
              POST:
                summary: ListCustomVocabularyItems
                description: >-
                  <p>Paginated list of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Lists
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
            /imports/:
              PUT:
                summary: StartImport
                description: >-
                  <p>Starts importing a bot, bot locale, or custom vocabulary
                  from a zip archive that you uploaded to an S3 bucket.</p>
                tags:
                  - Start
                  - Import
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
            /bots/{botId}/analytics/intentmetrics:
              POST:
                summary: ListIntentMetrics
                description: >-
                  <p>Retrieves summary metrics for the intents in your bot. The
                  following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsIntentMetric.html">AnalyticsIntentMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. You can specify
                  only one <code>order</code> in a given request.</p>
                tags:
                  - Lists
                  - Intent
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
            /bots/{botId}/analytics/intentpaths:
              POST:
                summary: ListIntentPaths
                description: >-
                  <p>Retrieves summary statistics for a path of intents that
                  users take over sessions with your bot. The following fields
                  are required:</p> <ul> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> <li> <p>
                  <code>intentPath</code> – Define an order of intents for which
                  you want to retrieve metrics. Separate intents in the path
                  with a forward slash. For example, populate the
                  <code>intentPath</code> field with
                  <code>/BookCar/BookHotel</code> to see details about how many
                  times users invoked the <code>BookCar</code> and
                  <code>BookHotel</code> intents in that order.</p> </li> </ul>
                  <p>Use the optional <code>filters</code> field to filter the
                  results.</p>
                tags:
                  - Lists
                  - Intent
                  - Paths
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
            /bots/{botId}/analytics/intentstagemetrics:
              POST:
                summary: ListIntentStageMetrics
                description: >-
                  <p>Retrieves summary metrics for the stages within intents in
                  your bot. The following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsIntentStageMetric.html">AnalyticsIntentStageMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. You can only
                  specify one <code>order</code> in a given request.</p>
                tags:
                  - Lists
                  - Intent
                  - Stage
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/intents:
              POST:
                summary: ListRecommendedIntents
                description: >-
                  <p>Gets a list of recommended intents provided by the bot
                  recommendation that you can use in your bot. Intents in the
                  response are ordered by relevance.</p>
                tags:
                  - Lists
                  - Recommended
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
            /bots/{botId}/analytics/sessions:
              POST:
                summary: ListSessionAnalyticsData
                description: >-
                  <p>Retrieves a list of metadata for individual user sessions
                  with your bot. The <code>startDateTime</code> and
                  <code>endDateTime</code> fields are required. These fields
                  define a time range for which you want to retrieve results. Of
                  the optional fields, you can organize the results in the
                  following ways:</p> <ul> <li> <p>Use the <code>filters</code>
                  field to filter the results and the <code>sortBy</code> field
                  to specify the values by which to sort the results.</p> </li>
                  <li> <p>Use the <code>maxResults</code> field to limit the
                  number of results to return in a single response and the
                  <code>nextToken</code> field to return the next batch of
                  results if the response does not return the full set of
                  results.</p> </li> </ul>
                tags:
                  - Lists
                  - Sessions
                  - Analytics
                  - Data
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
            /bots/{botId}/analytics/sessionmetrics:
              POST:
                summary: ListSessionMetrics
                description: >-
                  <p>Retrieves summary metrics for the user sessions with your
                  bot. The following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsSessionMetric.html">AnalyticsSessionMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. Currently, you
                  can specify it in either field, but not in both.</p>
                tags:
                  - Lists
                  - Sessions
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
            /tags/{resourceARN}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a bot, bot alias, or bot channel.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
            /testexecutions/{testExecutionId}/results:
              POST:
                summary: ListTestExecutionResultItems
                description: <p>Gets a list of test execution result items.</p>
                tags:
                  - Lists
                  - Tests
                  - Execution
                  - Results
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
            /testexecutions:
              POST:
                summary: ListTestExecutions
                description: <p>The list of test set executions.</p>
                tags:
                  - Lists
                  - Tests
                  - Executions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
            /testsets/{testSetId}/records:
              POST:
                summary: ListTestSetRecords
                description: <p>The list of test set records.</p>
                tags:
                  - Lists
                  - Tests
                  - Sets
                  - Records
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
            /testsets:
              POST:
                summary: ListTestSets
                description: <p>The list of the test sets</p>
                tags:
                  - Lists
                  - Tests
                  - Sets
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
            /bots/{botId}/analytics/utterances:
              POST:
                summary: ListUtteranceAnalyticsData
                description: >-
                  <note> <p>To use this API operation, your IAM role must have
                  permissions to perform the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, which provides access to utterance-related
                  analytics. See <a
                  href="https://docs.aws.amazon.com/lexv2/latest/dg/monitoring-utterances.html">Viewing
                  utterance statistics</a> for the IAM policy to apply to the
                  IAM role.</p> </note> <p>Retrieves a list of metadata for
                  individual user utterances to your bot. The following fields
                  are required:</p> <ul> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results and the <code>sortBy</code> field to
                  specify the values by which to sort the results.</p> </li>
                  <li> <p>Use the <code>maxResults</code> field to limit the
                  number of results to return in a single response and the
                  <code>nextToken</code> field to return the next batch of
                  results if the response does not return the full set of
                  results.</p> </li> </ul>
                tags:
                  - Lists
                  - Utterances
                  - Analytics
                  - Data
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
            /bots/{botId}/analytics/utterancemetrics:
              POST:
                summary: ListUtteranceMetrics
                description: >-
                  <note> <p>To use this API operation, your IAM role must have
                  permissions to perform the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, which provides access to utterance-related
                  analytics. See <a
                  href="https://docs.aws.amazon.com/lexv2/latest/dg/monitoring-utterances.html">Viewing
                  utterance statistics</a> for the IAM policy to apply to the
                  IAM role.</p> </note> <p>Retrieves summary metrics for the
                  utterances in your bot. The following fields are required:</p>
                  <ul> <li> <p> <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsUtteranceMetric.html">AnalyticsUtteranceMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. Currently, you
                  can specify it in either field, but not in both.</p>
                tags:
                  - Lists
                  - Utterances
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/associatedtranscripts:
              POST:
                summary: SearchAssociatedTranscripts
                description: >-
                  <p>Search for associated transcripts that meet the specified
                  criteria.</p>
                tags:
                  - Search
                  - Associated
                  - Transcripts
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/startgeneration:
              PUT:
                summary: StartBotResourceGeneration
                description: >-
                  <p>Starts a request for the descriptive bot builder to
                  generate a bot locale configuration based on the prompt you
                  provide it. After you make this call, use the
                  <code>DescribeBotResourceGeneration</code> operation to check
                  on the status of the generation and for the
                  <code>generatedBotLocaleUrl</code> when the generation is
                  complete. Use that value to retrieve the Amazon S3 object
                  containing the bot locale configuration. You can then modify
                  and import this configuration.</p>
                tags:
                  - Start
                  - Bot
                  - Resources
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
            /testsets/{testSetId}/testexecutions:
              POST:
                summary: StartTestExecution
                description: <p>The action to start test set execution.</p>
                tags:
                  - Start
                  - Tests
                  - Execution
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
            /testsetgenerations:
              PUT:
                summary: StartTestSetGeneration
                description: <p>The action to start the generation of test set.</p>
                tags:
                  - Start
                  - Tests
                  - Sets
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
                  - Test Set Generations
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/stopbotrecommendation:
              PUT:
                summary: StopBotRecommendation
                description: <p>Stop an already running Bot Recommendation re
                tags:
                  - Stop
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
                  - Test Set Generations
                  - Stopbotrecommendati
    overlays:
      - type: APIs.io Search
        url: overlays/modelslexv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/modelslexv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:modelslexv2
  - name: FactSet Benchmarks API
    description: >-
      Returns Benchmark Constituent data including weights, price, and market
      value for a specified date.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-benchmarks-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Benchmarks API
          paths:
            /factset-benchmarks/v1/constituents:
              get:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value. You must be authorized for
                  the `ids` requested. Use the helper endpoint **/id-list** for
                  valid identifiers.  
              post:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value. You must be authorized for
                  the `ids` requested. Use the helper endpoint **/id-list** for
                  valid identifiers.
            /factset-benchmarks/v1/fixed-income-constituents:
              get:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Fixed
                  - Income
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                summary: >-
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value.
                description: >
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value. You must be
                  authorized for the `ids` requested.
              post:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value. You must be
                  authorized for the `ids` requested.
            /factset-benchmarks/v1/index-snapshot:
              get:
                summary: >-
                  Index Level Prices, Returns, and related information as of a
                  single date.
                tags:
                  - Index
                  - Level
                  - Prices,
                  - Returns,
                  - And
                  - Related
                  - Information
                  - As
                  - Of
                  - Single
                  - Date.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                description: >
                  Retrieves Index Level Prices and Returns information as of a
                  specific date. Simply submit a valid Benchmark ID (you can use
                  the /id-list endpoint for a sample list of ids), and date and
                  retrieve Index Level Prices, Returns, and related information.
              post:
                summary: >-
                  Retrieves the Index Level Snapshot of Prices and Returns
                  information for a given identifier and single date.
                tags:
                  - Retrieves
                  - The
                  - Index
                  - Level
                  - Snapshot
                  - Of
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - Given
                  - Identifier
                  - Single
                  - Date.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                description: >
                  Retrieves Index Level Prices and Returns information as
                  aligned with FactSet's Benchmark Data Feed solution. Simply
                  submit a valid Benchmark ID (you can use the /id-list endpoint
                  for a sample list of ids), and date and retrieve Index Level
                  Prices, Returns, and related information.
            /factset-benchmarks/v1/index-history:
              get:
                summary: >-
                  Retrieves Index Level Prices and Returns information for a
                  list of identifiers and historical date range.
                tags:
                  - Retrieves
                  - Index
                  - Level
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Historical
                  - Date
                  - Range.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                description: >
                  Retrieves Index Level Prices and Returns information as of a
                  date range requested. Simply submit a valid Benchmark ID (you
                  can use the /id-list endpoint for a sample list of ids), and
                  date range to retrieve Index Level Prices, Returns, and
                  related information.
              post:
                summary: >-
                  Retrieves Index Level Prices and Returns information for a
                  list of identifiers and historical date range.
                tags:
                  - Retrieves
                  - Index
                  - Level
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Historical
                  - Date
                  - Range.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                description: >
                  Retrieves Index Level Prices and Returns information as
                  aligned with FactSet's Benchmark Data Feed solution. Simply
                  submit a valid Benchmark ID (you can use the /id-list endpoint
                  for a sample list of ids), and date and retrieve Index Level
                  Prices, Returns, and related information.
            /factset-benchmarks/v1/ratios:
              get:
                tags:
                  - Returns
                  - The
                  - Aggregated
                  - Ratios
                  - Of
                  - Requested
                  - Benchmark
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                summary: Returns the aggregated ratios of a requested benchmark
                description: >
                  Retrieves the index level ratios for a requested benchmark.
                  Ratios supported are expressed through metrics parameter, and
                  include Categories of Profitability, Valuation, Coverage, and
                  Leverage. <p> Using FactSet Market Aggregates, the service
                  combines fundamental, estimates, and pricing content to derive
                  ratios and per share values for global equity market indexes
                  and commercial benchmark vendors. The constituents of the
                  index are fetched on rolling basis over time period requested,
                  and then the metric requested is aggregated up to the index
                  level. To learn more about FMA, visit [OA
                  15778](https://my.apps.factset.com/oa/pages/15778).</p>
              post:
                tags:
                  - Returns
                  - The
                  - Aggregated
                  - Ratios
                  - Of
                  - Requested
                  - Benchmark
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                summary: Returns the aggregated ratios of a requested benchmark
                description: >
                  Retrieves the index level ratios for a requested benchmark.
                  Ratios supported are expressed through metrics parameter, and
                  include Categories of Profitability, Valuation, Coverage, and
                  Leverage. <p> Using FactSet Market Aggregates, the service
                  combines FactSet Fundamental, FactSet Estimates, and FactSet
                  Pricing content to derive ratios and per share values for
                  global equity market indexes and commercial benchmark vendors.
                  The constituents of the index are fetched on rolling basis
                  over time period requested, and then the metric requested is
                  aggregated up to the index level. To learn more about FMA,
                  visit [OA
                  15778](https://my.apps.factset.com/oa/pages/15778).</p>
            /factset-benchmarks/v1/id-list:
              get:
                summary: >-
                  Returns a sample list of Benchmark Identifiers and the
                  benchmark categorization to use in other Benchmark API
                  endpoints.
                tags:
                  - Returns
                  - Sample
                  - List
                  - Of
                  - Benchmark
                  - Identifiers
                  - And
                  - The
                  - Categorization
                  - To
                  - Use
                  - In
                  - Other
                  - Endpoints.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                  - Id
                  - List
                description: >-
                  Returns a **sample** list of Benchmark Identifiers to use in
                  other Benchmark API endpoints. This is a supporting API to be
                  use alongside the other Benchmark API endpoints. For example,
                  use the fsymID value returned in this response as the input to
                  your `ids` parameter in the /constituents endpoint to return
                  constituents for that id.<p> *This is not the full list of
                  benchmark ids allowed in this service, but rather a
                  representation of the most commonly requested. For complete
                  assistance with ID lookup or concordance services, please
                  reach out to FactSet Support. *</p>
              post:
                summary: >-
                  Returns a sample list of Benchmark Identifiers and the
                  benchmark categorization to use in other Benchmark API
                  endpoints.
                tags:
                  - Returns
                  - Sample
                  - List
                  - Of
                  - Benchmark
                  - Identifiers
                  - And
                  - The
                  - Categorization
                  - To
                  - Use
                  - In
                  - Other
                  - Endpoints.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                  - Id
                  - List
                description: >-
                  Returns a **sample** list of Benchmark Identifiers to use in
                  other Benchmark API endpoints. This is a supporting API to be
                  use alongside the other Benchmark API endpoints. For example,
                  use the fsymID value returned in this response as the input to
                  your `ids` parameter in the /constituents endpoint to return
                  constituents for that id.<p> *This is not the full list of
                  benchmark ids allowed in this service, but rather a
                  representation of the most commonly requested. For complete
                  assistance with ID lookup or concordance services, please
                  reach out to F
    overlays:
      - type: APIs.io Search
        url: overlays/benchmarks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/benchmarks-openapi-api-evangelist-ratings.yml
    aid: factset:factset-benchmarks-api
  - name: FactSet Real-Time Quotes API
    description: >-
      The Quotes API combines endpoints for retrieving security end-of-day,
      delayed, and realtime prices with performance key figures and basic
      reference data on the security and market level.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-quotes-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Quotes API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /basic/assetClass/list:
              get:
                tags:
                  - List
                  - Of
                  - Asset
                  - Classes.
                  - Class
                  - List
                description: List of asset classes as defined by FactSet Digital Solutions.
                summary: List of asset classes.
            /basic/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                summary: List of background text types.
                description: List of background text types.
            /basic/benchmark/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Benchmark
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                summary: List of benchmark types.
                description: List of benchmark types.
            /basic/delivery/list:
              post:
                tags:
                  - List
                  - Of
                  - Deliveries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                summary: List of deliveries.
                description: List of deliveries.
            /basic/frequency/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Frequency
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                summary: List of frequency types.
                description: List of frequency types.
            /basic/language/get:
              get:
                tags:
                  - Details
                  - For
                  - Language.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                description: Details for a language.
                summary: Details for a language.
            /basic/language/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Language
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: Details for a language identified by code.
                summary: Details for a language identified by code.
            /basic/language/list:
              get:
                tags:
                  - List
                  - Of
                  - Languages.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: List of languages.
                summary: List of languages.
            /basic/market/get:
              get:
                tags:
                  - Details
                  - Of
                  - Market.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: Details of a market.
                summary: Details of a market.
            /basic/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: List of markets.
                summary: List of markets.
            /basic/market/group/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Groups.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market groups.
                summary: List of market groups.
            /basic/market/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market types.
                summary: List of market types.
            /basic/media/kind/list:
              get:
                tags:
                  - List
                  - Of
                  - Media
                  - Kinds.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                summary: List of media kinds.
                description: List of media kinds.
            /basic/media/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Internet
                  - Media
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                description: >-
                  List of Internet media types. See
                  http://www.iana.org/assignments/media-types/ for further
                  details. Not all such Internet media types are available on
                  the MDG.
                summary: List of Internet media types.
            /basic/mic/operating/list:
              post:
                tags:
                  - List
                  - Of
                  - Operating
                  - Market
                  - Identifier
                  - Codes
                  - C).
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                summary: List of operating market identifier codes (MIC).
                description: List of operating market identifier codes (MIC).
            /basic/region/get:
              get:
                tags:
                  - Details
                  - For
                  - Region.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: Details for a region.
                description: Details for a geographic, political, or economic region.
            /basic/region/list:
              get:
                tags:
                  - List
                  - Of
                  - Regions.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: List of regions.
                description: List of geographic, political, and economic regions.
            /basic/region/continent/get:
              get:
                tags:
                  - Details
                  - For
                  - Continent.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: Details for a continent.
                description: Details for a continent.
            /basic/region/continent/list:
              get:
                tags:
                  - List
                  - Of
                  - Continents.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: List of continents.
                description: List of continents.
            /basic/region/country/get:
              get:
                tags:
                  - Details
                  - For
                  - Country.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country.
                description: Details for a country.
            /basic/region/country/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Country
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country identified by code.
                description: Details for a country identified by code.
            /basic/region/country/list:
              get:
                tags:
                  - List
                  - Of
                  - Countries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: List of countries.
                description: List of countries.
            /basic/timezone/get:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                description: >-
                  Details of a timezone identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone.
            /basic/timezone/getByName:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone
                  - Identified
                  - By
                  - Name.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  Details of a timezone identified by name, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone identified by name.
            /basic/timezone/list:
              post:
                tags:
                  - List
                  - Of
                  - Timezones.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  List of timezones identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: List of timezones.
            /basic/valueUnit/get:
              get:
                tags:
                  - Details
                  - Of
                  - Value
                  - Unit.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: Details of a value unit.
                description: Details of a value unit.
            /basic/valueUnit/list:
              post:
                tags:
                  - List
                  - Of
                  - Value
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: List of value units.
                description: List of value units.
            /basic/valueUnit/alternative/list:
              get:
                tags:
                  - List
                  - Of
                  - Alternative
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                description: List of alternative units.
                summary: List of alternative units.
            /basic/valueUnit/currency/list:
              post:
                tags:
                  - List
                  - Of
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                summary: List of currencies.
                description: List of currencies.
            /basic/valueUnit/currency/fractional/get:
              get:
                tags:
                  - Details
                  - Of
                  - Fractional
                  - Currency.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: Details of a fractional currency.
                description: Details of a fractional currency.
            /basic/valueUnit/currency/fractional/list:
              get:
                tags:
                  - List
                  - Of
                  - Fractional
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: List of fractional currencies.
                description: List of fractional currencies.
            /basic/valueUnit/currency/main/list:
              post:
                tags:
                  - List
                  - Of
                  - Main
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                summary: List of main currencies.
                description: List of main currencies.
            /category/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: Details of a category.
                description: Details of a category.
            /category/list:
              get:
                tags:
                  - List
                  - Of
                  - Categories.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: List of categories.
                description: List of categories.
            /category/listByLevel:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                summary: List of categories assigned to a category level.
                description: List of categories assigned to a category level.
            /category/listBySystem:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                summary: List of categories assigned to a category system.
                description: List of categories assigned to a category system.
            /category/dataset/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Datasets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                summary: List of entitled category datasets.
                description: List of entitled category datasets.
            /category/instrument/list:
              get:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Where
                  - Specific
                  - Dataset
                  - Has
                  - Assigned
                  - Given
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
                description: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
            /category/level/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: Details of a category level.
                description: Details of a category level.
            /category/path/get:
              get:
                tags:
                  - Path
                  - From
                  - The
                  - First
                  - Level
                  - To
                  - Of
                  - Specific
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Path from the first level to the level of a specific category.
                description: Path from the first level to the level of a specific category.
            /category/system/get:
              get:
                tags:
                  - Details
                  - Of
                  - An
                  - Entitled
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Details of an entitled category system.
                description: Details of an entitled category system.
            /category/system/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Systems.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of entitled category systems.
                description: List of entitled category systems.
            /category/system/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Category
                  - System
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of category system types.
                description: List of category system types.
            /instrument/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/getByNotation:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/backgroundText/list:
              get:
                tags:
                  - Background
                  - Texts
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: Background texts of an instrument.
                description: Background texts of an instrument.
            /instrument/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of background text types for instruments.
                description: List of background text types for instruments.
            /instrument/benchmark/list:
              post:
                tags:
                  - List
                  - Of
                  - Benchmarks
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of benchmarks of a financial instrument.
                description: >-
                  Provides a list of benchmark notations for a selected
                  financial instrument, optionally restricted to specific
                  benchmark types.
            /instrument/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Instrument
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see.
                description: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
            /instrument/complianceProperty/list:
              post:
                tags:
                  - List
                  - Of
                  - Compliance
                  - Properties
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: List of compliance properties for instruments.
                description: List of compliance properties for instruments.
            /instrument/complianceProperty/listByInstrument:
              get:
                tags:
                  - Compliance
                  - Properties
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: Compliance properties of an instrument.
                description: Compliance properties of an instrument.
            /instrument/composite/get:
              get:
                tags:
                  - Composite
                  - Instrument
                  - And
                  - Its
                  - Components.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                summary: Composite instrument and its components.
                description: Composite instrument and its components.
            /instrument/coupon/list:
              get:
                tags:
                  - List
                  - Of
                  - Coupons
                  - For
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                summary: List of coupons for an interest-bearing instrument.
                description: >-
                  List of coupons for an interest-bearing instrument; any other
                  instrument yields empty values. The endpoint provides details
                  regarding the coupon period, the respective interest rate, and
                  payable amount (the latter only for instruments with a fixed
                  nominal value). The list of coupons is generally not available
                  for a perpetual, i.e. without a predefined maturity date,
                  interst-bearing instrument. 


                  If there is no entitled provider supplying a full list of
                  coupons, the list will be synthesized from summary data
                  available from entitled suppliers (if any). Since the exact
                  product terms are not known, e.g. the handling of holidays and
                  weekends, the list may be imprecise.
            /instrument/coupon/dayCountConvention/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Day
                  - Count
                  - Convention
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                summary: List of day count convention types.
                description: List of day count convention types.
            /instrument/coupon/interestRate/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Interest
                  - Rate
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                summary: List of interest rate types.
                description: List of interest rate types.
            /instrument/coupon/keyData/get:
              get:
                tags:
                  - Interest
                  - Rate
                  - Details
                  - For
                  - Selected
                  - Periods
                  - Of
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                summary: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument.
                description: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument; any other instrument yields empty
                  values.
            /instrument/crossReference/getByISIN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given ISIN to the respective most recent
                  instrument identifier, retrieved from the Cross Reference
                  Service.
                summary: Translate ISIN to instrument.
            /instrument/crossReference/getByWKN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given WKN to the respective most recent instrument
                  identifier, retrieved from the Cross Reference Service.
                summary: Translate WKN to instrument.
            /instrument/crossReference/listByISIN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of ISINs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of ISINs to instruments.
            /instrument/crossReference/listByWKN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of WKNs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of WKNs to instruments.
            /instrument/crossReference/history/getByISIN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given ISIN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: ISIN to instrument translation history.
            /instrument/crossReference/history/getByWKN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given WKN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: WKN to instrument translation history.
            /instrument/exchangeRate/get:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the
                  identifier of the main currencies represented by that exchange
                  rate. 

                   An error is returned if one of the provided parameters is invalid or if no instrument is associated with the given combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/exchangeRate/getByISOCode:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the ISO
                  4217 code of the main currencies represented by that exchange
                  rate. 


                  An error is returned if one of the provided parameters is
                  invalid or if no instrument is associated with the given
                  combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/legalEntity/backgroundText/list:
              get:
                tags:
                  - Role-specific
                  - Background
                  - Texts
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                summary: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
                description: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
            /instrument/legalEntity/complianceProperty/list:
              get:
                tags:
                  - Role-specific
                  - Compliance
                  - Properties
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                summary: >-
                  Role-specific compliance properties of legal entities related
                  to an instrument.
                description: >-
                  Role-specic compliance properties of legal entities related to
                  an instrument.
            /instrument/mifid/get:
              get:
                tags:
                  - Mi
                  - Data
                  - For
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                description: >-
                  MiFID II data for a specified financial instrument. The
                  instruments governed by MiFID II are called "investment
                  products".
                summary: MiFID II data for a financial instrument.
            /instrument/notation/list:
              post:
                tags:
                  - List
                  - Of
                  - Active,
                  - Entitled
                  - Notations
                  - For
                  - Set
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                summary: List of active, entitled notations for a set of instruments.
                description: >-
                  List of active, entitled notations for a set of instruments.
                  By default the list of notations (per instrument) is sorted
                  descending by the trading volume, averaged over one month. All
                  identifiers used as parameters must be valid and entitled.
            /instrument/rating/grade/list:
              post:
                tags:
                  - List
                  - Of
                  - Rating
                  - Grades
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  List of rating grades for a list of instruments. The list can
                  be restricted to rating grades belonging to particular rating
                  systems.
                summary: List of rating grades for a list of instruments.
            /instrument/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Instrument-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: Set of custom instrument-level selection lists.
                summary: Set of custom instrument-level selection lists.
            /instrument/selectionList/listByInstrument:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Instrument,
                  - Returns
                  - The
                  - Instrument-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Instrument
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
                summary: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
            /instrument/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Belonging
                  - To
                  - An
                  - Instrument-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                summary: >-
                  List of instruments belonging to an instrument-level selection
                  list.
                description: >-
                  List of instruments belonging to an instrument-level selection
                  list.
            /notation/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a notation.
                summary: Basic data for a notation.
            /notation/list:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a list of notations.
                summary: Basic data for a list of notations.
            /notation/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Notation
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
                summary: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see.
            /notation/crossReference/getByFactSetMarketSymbol:
              get:
                tags:
                  - Translate
                  - Fact
                  - Set
                  - Market
                  - Symbol
                  - To
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: Translate a FactSet market symbol to a notation.
                description: >-
                  Translate a FactSet market symbol to a notation. This symbol
                  is also known as TICKER_EXCHANGE.
            /notation/crossReference/listByInstrument:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listByISIN:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listBySymbol:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: >-
                  List of entitled notations. Symbols are not globally unique;
                  therefore, a given symbol interpreted in different markets
                  might refer to different instruments.
            /notation/crossReference/factSetIdentifier/get:
              get:
                tags:
                  - Retrieve
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve FactSet identifiers for a given notation.
                description: >-
                  <p>Retrieve FactSet identifiers for a given notation. Security
                  and listing-level identifiers are always included, regional
                  level identifiers are included, if available.
            /notation/crossReference/factSetIdentifier/listByFactSetIdentifier:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Notations
                  - For
                  - Given
                  - Fact
                  - Set
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of notations for a given FactSet identifier.
                description: >-
                  <p>Retrieve a list of notations for a given FactSet
                  identifier, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>See the group
                  description for more information about the security's primary
                  listing.</p>
            /notation/crossReference/factSetIdentifier/listByInstrument:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of FactSet identifiers for a given instrument.
                description: >-
                  <p>Retrieve a list of FactSet identifiers for a given
                  instrument, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>The result
                  contains only notations that have at least one FactSet
                  identifier (see
                  <big><tt>listing.permanentIdentifier</tt></big>,
                  <big><tt>listing.tickerExchange</tt></big>).</p><p>See the
                  group description for more information about the security's
                  primary listing.</p>
            /notation/keyFigures/year/10/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: End-of-day (EOD) key figures for the time range of ten years.
                description: End-of-day (EOD) key figures for the time range of ten years.
            /notation/keyFigures/year/10/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
            /notation/keyFigures/month/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: End-of-day (EOD) key figures for the time range of one month.
                description: End-of-day (EOD) key figures for the time range of one month.
            /notation/keyFigures/month/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
            /notation/keyFigures/week/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one week.
                description: End-of-day (EOD) key figures for the time range of one week.
            /notation/keyFigures/week/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
            /notation/keyFigures/year/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one year.
                description: End-of-day (EOD) key figures for the time range of one year.
            /notation/keyFigures/year/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
            /notation/keyFigures/month/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
            /notation/keyFigures/month/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
            /notation/keyFigures/year/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
            /notation/keyFigures/year/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
            /notation/keyFigures/year/5/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of five years.
                description: End-of-day (EOD) key figures for the time range of five years.
            /notation/keyFigures/year/5/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
            /notation/keyFigures/month/6/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of six months.
                description: End-of-day (EOD) key figures for the time range of six months.
            /notation/keyFigures/month/6/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
            /notation/keyFigures/year/7/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
            /notation/keyFigures/year/7/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
            /notation/keyFigures/yearToDate/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D)..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD)..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD). The time range YTD begins with the last trading day of
                  the previous calendar year for which EOD prices are available
                  and ends with the most recent trading day of the current
                  calendar year for which EOD prices are available..
            /notation/keyFigures/yearToDate/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D),
                  - List
                  - Of
                  - Notations..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations. The time range YTD begins with
                  the last trading day of the previous calendar year for which
                  EOD prices are available and ends with the most recent
                  tradingday of the current calendar year for which EOD prices
                  are available..
            /notation/keyFigures/tradingDay/average/get:
              get:
                tags:
                  - Average
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - Different
                  - Trading
                  - Days
                  - Periods.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods. A trading day is a calendar day on that trading
                  of the notation was possible.
                summary: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods.
            /notation/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets
                  - With
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  List of markets with entitled notations. The list contains
                  only markets with at least one active and entitled notation. 

                  All identifiers used as parameters must be valid and entitled.
                summary: List of markets with entitled notations.
            /notation/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Notation-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: Set of custom notation-level selection lists.
                summary: Set of custom notation-level selection lists.
            /notation/selectionList/listByNotation:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Notation,
                  - Returns
                  - The
                  - Notation-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Notation
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
                summary: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
            /notation/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Notations
                  - Belonging
                  - To
                  - Notation-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                summary: >-
                  List of notations belonging to a notation-level selection
                  list.
                description: >-
                  List of notations belonging to a notation-level selection
                  list.
            /notation/status/get:
              get:
                tags:
                  - Intraday
                  - Trading
                  - Status
                  - Of
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                description: >-
                  Intraday trading status of a notation.<br>The endpoint is
                  subscribable to provide push updates. See attribute
                  `_subscriptionMinimalInterval` for valid update rates.
                summary: Intraday trading status of a notation.
            /prices/get:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/list:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
            /prices/bidAsk/get:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/bidAsk/list:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
            /prices/orderbook/aggregated/get:
              get:
                tags:
                  - Orderbook
                  - Aggregated
                  - By
                  - Price.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                summary: Orderbook aggregated by price.
                description: Orderbook aggregated by price.
            /prices/orderbook/full/get:
              get:
                tags:
                  - Full
                  - Orderbook
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                summary: Full orderbook
                description: Full orderbook
            /prices/tradingSchedule/event/list:
              post:
                tags:
                  - Sequence
                  - Of
                  - Market-related
                  - Events.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Sequence of market-related events.
                description: >-
                  Sequence of market-related events like the opening time or
                  closing time of a market of a specific
                  notation.<br><br>Pagination to a previous page is not
                  supported and `pagination.previous` is always `null`.
            /prices/tradingSchedule/event/type/list:
              get:
                tags:
                  - Trading
                  - Schedule
                  - Event
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Trading schedule event types.
                description: >-
                  Trading schedule event types define the events which may occur
                  during any period of trading. Types of trading schedule events
                  are for instance OPEN, CLOSE, END_OF_DAY.
            /instrument/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for instruments.
                description: >-
                  Search for instruments whose ISIN, specified NSINs, or name
                  match the search value according to a tolerant full-text match
                  algorithm. Better matching results appear in the response
                  before less relevant matches.
            /notation/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for notations.
                description: >-
                  Search for a notation whose ISIN, specified NSINs, name, or
                  symbol match the search value according to a tolerant
                  full-text match algorithm. If more than one notation of an
                  instrument matches, only the notation with the highest
                  monetary trading volume, averaged over one month, is
                  considered. Better matching results appear in the response
                  before less relevant matches. If the parameter popularity is
                  set to true, the popularity of the notation is the primary
                  sort criterion. Popularity is affected mostly by the request
                  frequency of the notation.
            /notation/searchByText:
              post:
                tags:
                  - Text-based
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Text-based search for notations.
                description: >-
                  Text-based search for notations in selected identifier and
                  name attributes according to a tolerant full-text match
                  algorithm. The results satisfy all selected filters; sorting
                  by various attributes is possible. If more than one notation
                  of an instrument matches, only the notation with the best
                  market priority (according to the parameter `market.priority`)
                  or, in the absence of market priorities, only the notation
                  with the highest trading volume, averaged over one month, is
                  considered.     
                   All identifiers used as parameters must be valid and entitled.
          tags:
            - name: basic
              description: basic endpoints
            - name: category
              description: category endpoints
            - name: instrument
              description: instrument endpoints
            - name: notation
              description: notation endpoints
            - name: prices
              description: prices endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-quotes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-quotes-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-quotes-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---