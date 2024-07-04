---
name: Backup
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/backup.png
url: https://example.com/apis/backup.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Backup
apis:
  - name: backup
    description: >-
      <fullname>Backup</fullname> <p>Backup is a unified backup service designed
      to protect Amazon Web Services services and their associated data. Backup
      simplifies the creation, migration, restoration, and deletion of backups,
      while also providing reporting and auditing.</p>
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
            title: backup
          paths:
            /legal-holds/{legalHoldId}:
              DELETE:
                summary: CancelLegalHold
                description: >-
                  <p>This action removes the specified legal hold on a recovery
                  point. This action can only be performed by a user with
                  sufficient permissions.</p>
                tags:
                  - Cancel
                  - Legal
                  - Hold
                  - Hold
                  - Identifiers
            /backup/plans/:
              GET:
                summary: ListBackupPlans
                description: >-
                  <p>Returns a list of all active backup plans for an
                  authenticated account. The list contains information such as
                  Amazon Resource Names (ARNs), plan IDs, creation and deletion
                  dates, version IDs, plan names, and creator request IDs.</p>
                tags:
                  - Lists
                  - Backup
                  - Plans
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
            /backup/plans/{backupPlanId}/selections/:
              GET:
                summary: ListBackupSelections
                description: >-
                  <p>Returns an array containing metadata of the resources
                  associated with the target backup plan.</p>
                tags:
                  - Lists
                  - Backup
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
            /backup-vaults/{backupVaultName}:
              GET:
                summary: DescribeBackupVault
                description: >-
                  <p>Returns metadata about a backup vault specified by its
                  name.</p>
                tags:
                  - Describe
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
            /audit/frameworks:
              GET:
                summary: ListFrameworks
                description: >-
                  <p>Returns a list of all frameworks for an Amazon Web Services
                  account and Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Frameworks
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
            /legal-holds/:
              GET:
                summary: ListLegalHolds
                description: >-
                  <p>This action returns metadata about active and previous
                  legal holds.</p>
                tags:
                  - Lists
                  - Legal
                  - Holds
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
            /logically-air-gapped-backup-vaults/{backupVaultName}:
              PUT:
                summary: CreateLogicallyAirGappedBackupVault
                description: >-
                  <p>This request creates a logical container to where backups
                  may be copied.</p> <p>This request includes a name, the
                  Region, the maximum number of retention days, the minimum
                  number of retention days, and optionally can include tags and
                  a creator request ID.</p> <note> <p>Do not include sensitive
                  data, such as passport numbers, in the name of a backup
                  vault.</p> </note>
                tags:
                  - Create
                  - Logically
                  - Air
                  - Gapped
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
            /audit/report-plans:
              GET:
                summary: ListReportPlans
                description: >-
                  <p>Returns a list of your report plans. For detailed
                  information about a single report plan, use
                  <code>DescribeReportPlan</code>.</p>
                tags:
                  - Lists
                  - Reports
                  - Plans
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
            /restore-testing/plans:
              GET:
                summary: ListRestoreTestingPlans
                description: <p>Returns a list of restore testing plans.</p>
                tags:
                  - Lists
                  - Restore
                  - Testing
                  - Plans
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
            /restore-testing/plans/{RestoreTestingPlanName}/selections:
              GET:
                summary: ListRestoreTestingSelections
                description: >-
                  <p>Returns a list of restore testing selections. Can be
                  filtered by <code>MaxResults</code> and
                  <code>RestoreTestingPlanName</code>.</p>
                tags:
                  - Lists
                  - Restore
                  - Testing
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
            /backup/plans/{backupPlanId}:
              POST:
                summary: UpdateBackupPlan
                description: >-
                  <p>Updates an existing backup plan identified by its
                  <code>backupPlanId</code> with the input document in JSON
                  format. The new version is uniquely identified by a
                  <code>VersionId</code>.</p>
                tags:
                  - Update
                  - Backup
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
            /backup/plans/{backupPlanId}/selections/{selectionId}:
              GET:
                summary: GetBackupSelection
                description: >-
                  <p>Returns selection metadata and a document in JSON format
                  that specifies a list of resources that are associated with a
                  backup plan.</p>
                tags:
                  - Get
                  - Backup
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
            /backup-vaults/{backupVaultName}/access-policy:
              PUT:
                summary: PutBackupVaultAccessPolicy
                description: >-
                  <p>Sets a resource-based policy that is used to manage access
                  permissions on the target backup vault. Requires a backup
                  vault name and an access policy document in JSON format.</p>
                tags:
                  - Put
                  - Backup
                  - Vault
                  - Access
                  - Policies
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
            /backup-vaults/{backupVaultName}/vault-lock:
              PUT:
                summary: PutBackupVaultLockConfiguration
                description: >-
                  <p>Applies Backup Vault Lock to a backup vault, preventing
                  attempts to delete any recovery point stored in or created in
                  a backup vault. Vault Lock also prevents attempts to update
                  the lifecycle policy that controls the retention period of any
                  recovery point currently stored in a backup vault. If
                  specified, Vault Lock enforces a minimum and maximum retention
                  period for future backup and copy jobs that target a backup
                  vault.</p> <note> <p>Backup Vault Lock has been assessed by
                  Cohasset Associates for use in environments that are subject
                  to SEC 17a-4, CFTC, and FINRA regulations. For more
                  information about how Backup Vault Lock relates to these
                  regulations, see the <a
                  href="samples/cohassetreport.zip">Cohasset Associates
                  Compliance Assessment.</a> </p> </note>
                tags:
                  - Put
                  - Backup
                  - Vault
                  - Locks
                  - Configurations
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
            /backup-vaults/{backupVaultName}/notification-configuration:
              PUT:
                summary: PutBackupVaultNotifications
                description: >-
                  <p>Turns on notifications on a backup vault for the specified
                  topic and events.</p>
                tags:
                  - Put
                  - Backup
                  - Vault
                  - Notifications
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
            /audit/frameworks/{frameworkName}:
              PUT:
                summary: UpdateFramework
                description: >-
                  <p>Updates an existing framework identified by its
                  <code>FrameworkName</code> with the input document in JSON
                  format.</p>
                tags:
                  - Update
                  - Frameworks
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}:
              POST:
                summary: UpdateRecoveryPointLifecycle
                description: >-
                  <p>Sets the transition lifecycle of a recovery point.</p>
                  <p>The lifecycle defines when a protected resource is
                  transitioned to cold storage and when it expires. Backup
                  transitions and expires backups automatically according to the
                  lifecycle that you define.</p> <p>Backups transitioned to cold
                  storage must be stored in cold storage for a minimum of 90
                  days. Therefore, the “retention” setting must be 90 days
                  greater than the “transition to cold after days” setting. The
                  “transition to cold after days” setting cannot be changed
                  after a backup has been transitioned to cold.</p> <p>Resource
                  types that are able to be transitioned to cold storage are
                  listed in the "Lifecycle to cold storage" section of the <a
                  href="https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html#features-by-resource">
                  Feature availability by resource</a> table. Backup ignores
                  this expression for other resource types.</p> <p>This
                  operation does not support continuous backups.</p>
                tags:
                  - Update
                  - Recovery
                  - Points
                  - Lifecycle
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /audit/report-plans/{reportPlanName}:
              PUT:
                summary: UpdateReportPlan
                description: >-
                  <p>Updates an existing report plan identified by its
                  <code>ReportPlanName</code> with the input document in JSON
                  format.</p>
                tags:
                  - Update
                  - Reports
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /restore-testing/plans/{RestoreTestingPlanName}:
              PUT:
                summary: UpdateRestoreTestingPlan
                description: >-
                  <p>This request will send changes to your specified restore
                  testing plan. <code>RestoreTestingPlanName</code> cannot be
                  updated after it is created.</p> <p>
                  <code>RecoveryPointSelection</code> can contain:</p> <ul> <li>
                  <p> <code>Algorithm</code> </p> </li> <li> <p>
                  <code>ExcludeVaults</code> </p> </li> <li> <p>
                  <code>IncludeVaults</code> </p> </li> <li> <p>
                  <code>RecoveryPointTypes</code> </p> </li> <li> <p>
                  <code>SelectionWindowDays</code> </p> </li> </ul>
                tags:
                  - Update
                  - Restore
                  - Testing
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /restore-testing/plans/{RestoreTestingPlanName}/selections/{RestoreTestingSelectionName}:
              PUT:
                summary: UpdateRestoreTestingSelection
                description: >-
                  <p>Most elements except the
                  <code>RestoreTestingSelectionName</code> can be updated with
                  this request.</p> <p> <code>RestoreTestingSelection</code> can
                  use either protected resource ARNs or conditions, but not
                  both. That is, if your selection has
                  <code>ProtectedResourceArns</code>, requesting an update with
                  the parameter <code>ProtectedResourceConditions</code> will be
                  unsuccessful.</p>
                tags:
                  - Update
                  - Restore
                  - Testing
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /backup-jobs/{backupJobId}:
              POST:
                summary: StopBackupJob
                description: >-
                  <p>Attempts to cancel a job to create a one-time backup of a
                  resource.</p> <p>This action is not supported for the
                  following services: Amazon FSx for Windows File Server, Amazon
                  FSx for Lustre, FSx for ONTAP , Amazon FSx for OpenZFS, Amazon
                  DocumentDB (with MongoDB compatibility), Amazon RDS, Amazon
                  Aurora, and Amazon Neptune.</p>
                tags:
                  - Stop
                  - Backup
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
            /copy-jobs/{copyJobId}:
              GET:
                summary: DescribeCopyJob
                description: >-
                  <p>Returns metadata associated with creating a copy of a
                  resource.</p>
                tags:
                  - Describe
                  - Copy
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
            /global-settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates whether the Amazon Web Services account is opted in
                  to cross-account backup. Returns an error if the account is
                  not an Organizations management account. Use the
                  <code>DescribeGlobalSettings</code> API to determine the
                  current settings.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
            /resources/{resourceArn}:
              GET:
                summary: DescribeProtectedResource
                description: >-
                  <p>Returns information about a saved resource, including the
                  last time it was backed up, its Amazon Resource Name (ARN),
                  and the Amazon Web Services service type of the saved
                  resource.</p>
                tags:
                  - Describe
                  - Protected
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
            /account-settings:
              PUT:
                summary: UpdateRegionSettings
                description: >-
                  <p>Updates the current service opt-in settings for the
                  Region.</p> <p>Use the <code>DescribeRegionSettings</code> API
                  to determine the resource types that are supported.</p>
                tags:
                  - Update
                  - Regions
                  - Settings
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
            /audit/report-jobs/{reportJobId}:
              GET:
                summary: DescribeReportJob
                description: >-
                  <p>Returns the details associated with creating a report as
                  specified by its <code>ReportJobId</code>.</p>
                tags:
                  - Describe
                  - Reports
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
            /restore-jobs/{restoreJobId}:
              GET:
                summary: DescribeRestoreJob
                description: >-
                  <p>Returns metadata associated with a restore job that is
                  specified by a job ID.</p>
                tags:
                  - Describe
                  - Restore
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}/disassociate:
              POST:
                summary: DisassociateRecoveryPoint
                description: >-
                  <p>Deletes the specified continuous backup recovery point from
                  Backup and releases control of that continuous backup to the
                  source service, such as Amazon RDS. The source service will
                  continue to create and retain continuous backups using the
                  lifecycle that you specified in your original backup plan.</p>
                  <p>Does not support snapshot backup recovery points.</p>
                tags:
                  - Disassociate
                  - Recovery
                  - Points
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}/parentAssociation:
              DELETE:
                summary: DisassociateRecoveryPointFromParent
                description: >-
                  <p>This action to a specific child (nested) recovery point
                  removes the relationship between the specified recovery point
                  and its parent (composite) recovery point.</p>
                tags:
                  - Disassociate
                  - Recovery
                  - Points
                  - From
                  - Parents
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
            /backup/plans/{backupPlanId}/toTemplate/:
              GET:
                summary: ExportBackupPlanTemplate
                description: >-
                  <p>Returns the backup plan that is specified by the plan ID as
                  a backup template.</p>
                tags:
                  - Export
                  - Backup
                  - Plan
                  - Templates
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup/plans/{backupPlanId}/:
              GET:
                summary: GetBackupPlan
                description: >-
                  <p>Returns <code>BackupPlan</code> details for the specified
                  <code>BackupPlanId</code>. The details are the body of a
                  backup plan in JSON format, in addition to plan metadata.</p>
                tags:
                  - Get
                  - Backup
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup/template/json/toPlan:
              POST:
                summary: GetBackupPlanFromJSON
                description: >-
                  <p>Returns a valid JSON document specifying a backup plan or
                  an error.</p>
                tags:
                  - Get
                  - Backup
                  - Plan
                  - From
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup/template/plans/{templateId}/toPlan:
              GET:
                summary: GetBackupPlanFromTemplate
                description: >-
                  <p>Returns the template specified by its
                  <code>templateId</code> as a backup plan.</p>
                tags:
                  - Get
                  - Backup
                  - Plan
                  - From
                  - Templates
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /legal-holds/{legalHoldId}/:
              GET:
                summary: GetLegalHold
                description: >-
                  <p>This action returns details for a specified legal hold. The
                  details are the body of a legal hold in JSON format, in
                  addition to metadata.</p>
                tags:
                  - Get
                  - Legal
                  - Hold
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}/restore-metadata:
              GET:
                summary: GetRecoveryPointRestoreMetadata
                description: >-
                  <p>Returns a set of metadata key-value pairs that were used to
                  create the backup.</p>
                tags:
                  - Get
                  - Recovery
                  - Points
                  - Restore
                  - Metadata
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
            /restore-jobs/{restoreJobId}/metadata:
              GET:
                summary: GetRestoreJobMetadata
                description: >-
                  <p>This request returns the metadata for the specified restore
                  job.</p>
                tags:
                  - Get
                  - Restore
                  - Jobs
                  - Metadata
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
            /restore-testing/inferred-metadata:
              GET:
                summary: GetRestoreTestingInferredMetadata
                description: >-
                  <p>This request returns the minimal required set of metadata
                  needed to start a restore job with secure default settings.
                  <code>BackupVaultName</code> and <code>RecoveryPointArn</code>
                  are required parameters. <code>BackupVaultAccountId</code> is
                  an optional parameter.</p>
                tags:
                  - Get
                  - Restore
                  - Testing
                  - Inferred
                  - Metadata
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
            /supported-resource-types:
              GET:
                summary: GetSupportedResourceTypes
                description: >-
                  <p>Returns the Amazon Web Services resource types supported by
                  Backup.</p>
                tags:
                  - Get
                  - Supported
                  - Resources
                  - Types
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
            /audit/backup-job-summaries:
              GET:
                summary: ListBackupJobSummaries
                description: >-
                  <p>This is a request for a summary of backup jobs created or
                  running within the most recent 30 days. You can include
                  parameters AccountID, State, ResourceType, MessageCategory,
                  AggregationPeriod, MaxResults, or NextToken to filter
                  results.</p> <p>This request returns a summary that contains
                  Region, Account, State, ResourceType, MessageCategory,
                  StartTime, EndTime, and Count of included jobs.</p>
                tags:
                  - Lists
                  - Backup
                  - Jobs
                  - Summaries
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
            /backup-jobs/:
              GET:
                summary: ListBackupJobs
                description: >-
                  <p>Returns a list of existing backup jobs for an authenticated
                  account for the last 30 days. For a longer period of time,
                  consider using these <a
                  href="https://docs.aws.amazon.com/aws-backup/latest/devguide/monitoring.html">monitoring
                  tools</a>.</p>
                tags:
                  - Lists
                  - Backup
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
            /backup/template/plans:
              GET:
                summary: ListBackupPlanTemplates
                description: >-
                  <p>Returns metadata of your saved backup plan templates,
                  including the template ID, name, and the creation and deletion
                  dates.</p>
                tags:
                  - Lists
                  - Backup
                  - Plan
                  - Templates
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
            /backup/plans/{backupPlanId}/versions/:
              GET:
                summary: ListBackupPlanVersions
                description: >-
                  <p>Returns version metadata of your backup plans, including
                  Amazon Resource Names (ARNs), backup plan IDs, creation and
                  deletion dates, plan names, and version IDs.</p>
                tags:
                  - Lists
                  - Backup
                  - Plan
                  - Versions
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
            /backup-vaults/:
              GET:
                summary: ListBackupVaults
                description: >-
                  <p>Returns a list of recovery point storage containers along
                  with information about them.</p>
                tags:
                  - Lists
                  - Backup
                  - Vaults
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
            /audit/copy-job-summaries:
              GET:
                summary: ListCopyJobSummaries
                description: >-
                  <p>This request obtains a list of copy jobs created or running
                  within the the most recent 30 days. You can include parameters
                  AccountID, State, ResourceType, MessageCategory,
                  AggregationPeriod, MaxResults, or NextToken to filter
                  results.</p> <p>This request returns a summary that contains
                  Region, Account, State, RestourceType, MessageCategory,
                  StartTime, EndTime, and Count of included jobs.</p>
                tags:
                  - Lists
                  - Copy
                  - Jobs
                  - Summaries
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
            /copy-jobs/:
              GET:
                summary: ListCopyJobs
                description: <p>Returns metadata about your copy jobs.</p>
                tags:
                  - Lists
                  - Copy
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
            /resources/:
              GET:
                summary: ListProtectedResources
                description: >-
                  <p>Returns an array of resources successfully backed up by
                  Backup, including the time the resource was saved, an Amazon
                  Resource Name (ARN) of the resource, and a resource type.</p>
                tags:
                  - Lists
                  - Protected
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /backup-vaults/{backupVaultName}/resources/:
              GET:
                summary: ListProtectedResourcesByBackupVault
                description: >-
                  <p>This request lists the protected resources corresponding to
                  each backup vault.</p>
                tags:
                  - Lists
                  - Protected
                  - Resources
                  - By
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /backup-vaults/{backupVaultName}/recovery-points/:
              GET:
                summary: ListRecoveryPointsByBackupVault
                description: >-
                  <p>Returns detailed information about the recovery points
                  stored in a backup vault.</p>
                tags:
                  - Lists
                  - Recovery
                  - Points
                  - By
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /legal-holds/{legalHoldId}/recovery-points:
              GET:
                summary: ListRecoveryPointsByLegalHold
                description: >-
                  <p>This action returns recovery point ARNs (Amazon Resource
                  Names) of the specified legal hold.</p>
                tags:
                  - Lists
                  - Recovery
                  - Points
                  - By
                  - Legal
                  - Hold
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /resources/{resourceArn}/recovery-points/:
              GET:
                summary: ListRecoveryPointsByResource
                description: >-
                  <p>Returns detailed information about all the recovery points
                  of the type specified by a resource Amazon Resource Name
                  (ARN).</p> <note> <p>For Amazon EFS and Amazon EC2, this
                  action only lists recovery points created by Backup.</p>
                  </note>
                tags:
                  - Lists
                  - Recovery
                  - Points
                  - By
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /audit/report-jobs:
              GET:
                summary: ListReportJobs
                description: <p>Returns details about your report jobs.</p>
                tags:
                  - Lists
                  - Reports
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /audit/restore-job-summaries:
              GET:
                summary: ListRestoreJobSummaries
                description: >-
                  <p>This request obtains a summary of restore jobs created or
                  running within the the most recent 30 days. You can include
                  parameters AccountID, State, ResourceType, AggregationPeriod,
                  MaxResults, or NextToken to filter results.</p> <p>This
                  request returns a summary that contains Region, Account,
                  State, RestourceType, MessageCategory, StartTime, EndTime, and
                  Count of included jobs.</p>
                tags:
                  - Lists
                  - Restore
                  - Jobs
                  - Summaries
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /restore-jobs/:
              GET:
                summary: ListRestoreJobs
                description: >-
                  <p>Returns a list of jobs that Backup initiated to restore a
                  saved resource, including details about the recovery
                  process.</p>
                tags:
                  - Lists
                  - Restore
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /resources/{resourceArn}/restore-jobs/:
              GET:
                summary: ListRestoreJobsByProtectedResource
                description: >-
                  <p>This returns restore jobs that contain the specified
                  protected resource.</p> <p>You must include
                  <code>ResourceArn</code>. You can optionally include
                  <code>NextToken</code>, <code>ByStatus</code>,
                  <code>MaxResults</code>,
                  <code>ByRecoveryPointCreationDateAfter</code> , and
                  <code>ByRecoveryPointCreationDateBefore</code>.</p>
                tags:
                  - Lists
                  - Restore
                  - Jobs
                  - By
                  - Protected
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /tags/{resourceArn}/:
              GET:
                summary: ListTags
                description: >-
                  <p>Returns a list of key-value pairs assigned to a target
                  recovery point, backup plan, or backup vault.</p> <p>
                  <code>ListTags</code> only works for resource types that
                  support full Backup management of their backups. Those
                  resource types are listed in the "Full Backup management"
                  section of the <a
                  href="https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html#features-by-resource">
                  Feature availability by resource</a> table.</p>
                tags:
                  - Lists
                  - Tags
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /restore-jobs/{restoreJobId}/validations:
              PUT:
                summary: PutRestoreValidationResult
                description: >-
                  <p>This request allows you to send your independent self-run
                  restore test validation results. <code>RestoreJobId</code> and
                  <code>ValidationStatus</code> are required. Optionally, you
                  can input a <code>ValidationStatusMessage</code>.</p>
                tags:
                  - Put
                  - Restore
                  - Validations
                  - Results
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /backup-jobs:
              PUT:
                summary: StartBackupJob
                description: >-
                  <p>Starts an on-demand backup job for the specified
                  resource.</p>
                tags:
                  - Start
                  - Backup
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /copy-jobs:
              PUT:
                summary: StartCopyJob
                description: >-
                  <p>Starts a job to create a one-time copy of the specified
                  resource.</p> <p>Does not support continuous backups.</p>
                tags:
                  - Start
                  - Copy
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /audit/report-jobs/{reportPlanName}:
              POST:
                summary: StartReportJob
                description: >-
                  <p>Starts an on-demand report job for the specified report
                  plan.</p>
                tags:
                  - Start
                  - Reports
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /restore-jobs:
              PUT:
                summary: StartRestoreJob
                description: >-
                  <p>Recovers the saved resource identified by an Amazon
                  Resource Name (ARN).</p>
                tags:
                  - Start
                  - Restore
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /tags/{resourceArn}:
              POST:
                summary: TagResource
                description: >-
                  <p>Assigns a set of key-value pairs to a recovery point,
                  backup plan, or backup vault identified by an Amazon Resource
                  Name (ARN).</p>
                tags:
                  - Tags
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /untag/{resourceArn}:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes a set of key-value pairs from a recovery point,
                  backup plan, or backup vault identified by an Amazon Resource
                  Name
                tags:
                  - Untag
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
    overlays:
      - type: APIs.io Search
        url: overlays/backup-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/backup-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:backup
  - name: elasticfilesystem
    description: >-
      <fullname>Amazon Elastic File System</fullname> <p>Amazon Elastic File
      System (Amazon EFS) provides simple, scalable file storage for use with
      Amazon EC2 Linux and Mac instances in the Amazon Web Services Cloud. With
      Amazon EFS, storage capacity is elastic, growing and shrinking
      automatically as you add and remove files, so that your applications have
      the storage they need, when they need it. For more information, see the <a
      href="https://docs.aws.amazon.com/efs/latest/ug/api-reference.html">Amazon
      Elastic File System API Reference</a> and the <a
      href="https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html">Amazon
      Elastic File System User Guide</a>.</p>
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
            title: elasticfilesystem
          paths:
            /2015-02-01/access-points:
              GET:
                summary: DescribeAccessPoints
                description: >-
                  <p>Returns the description of a specific Amazon EFS access
                  point if the <code>AccessPointId</code> is provided. If you
                  provide an EFS <code>FileSystemId</code>, it returns
                  descriptions of all access points for that file system. You
                  can provide either an <code>AccessPointId</code> or a
                  <code>FileSystemId</code> in the request, but not both. </p>
                  <p>This operation requires permissions for the
                  <code>elasticfilesystem:DescribeAccessPoints</code>
                  action.</p>
                tags:
                  - Describe
                  - Access
                  - Points
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
            /2015-02-01/file-systems:
              GET:
                summary: DescribeFileSystems
                description: >-
                  <p>Returns the description of a specific Amazon EFS file
                  system if either the file system <code>CreationToken</code> or
                  the <code>FileSystemId</code> is provided. Otherwise, it
                  returns descriptions of all file systems owned by the caller's
                  Amazon Web Services account in the Amazon Web Services Region
                  of the endpoint that you're calling.</p> <p>When retrieving
                  all file system descriptions, you can optionally specify the
                  <code>MaxItems</code> parameter to limit the number of
                  descriptions in a response. This number is automatically set
                  to 100. If more file system descriptions remain, Amazon EFS
                  returns a <code>NextMarker</code>, an opaque token, in the
                  response. In this case, you should send a subsequent request
                  with the <code>Marker</code> request parameter set to the
                  value of <code>NextMarker</code>. </p> <p>To retrieve a list
                  of your file system descriptions, this operation is used in an
                  iterative process, where <code>DescribeFileSystems</code> is
                  called first without the <code>Marker</code> and then the
                  operation continues to call it with the <code>Marker</code>
                  parameter set to the value of the <code>NextMarker</code> from
                  the previous response until the response has no
                  <code>NextMarker</code>. </p> <p> The order of file systems
                  returned in the response of one
                  <code>DescribeFileSystems</code> call and the order of file
                  systems returned across the responses of a multi-call
                  iteration is unspecified. </p> <p> This operation requires
                  permissions for the
                  <code>elasticfilesystem:DescribeFileSystems</code> action.
                  </p>
                tags:
                  - Describe
                  - File
                  - Systems
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
            /2015-02-01/mount-targets:
              GET:
                summary: DescribeMountTargets
                description: >-
                  <p>Returns the descriptions of all the current mount targets,
                  or a specific mount target, for a file system. When requesting
                  all of the current mount targets, the order of mount targets
                  returned in the response is unspecified.</p> <p>This operation
                  requires permissions for the
                  <code>elasticfilesystem:DescribeMountTargets</code> action, on
                  either the file system ID that you specify in
                  <code>FileSystemId</code>, or on the file system of the mount
                  target that you specify in <code>MountTargetId</code>.</p>
                tags:
                  - Describe
                  - Mount
                  - Targets
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
            /2015-02-01/file-systems/{SourceFileSystemId}/replication-configuration:
              DELETE:
                summary: DeleteReplicationConfiguration
                description: >-
                  <p>Deletes a replication configuration. Deleting a replication
                  configuration ends the replication process. After a
                  replication configuration is deleted, the destination file
                  system becomes <code>Writeable</code> and its replication
                  overwrite protection is re-enabled. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/efs/latest/ug/delete-replications.html">Delete
                  a replication configuration</a>.</p> <p>This operation
                  requires permissions for the
                  <code>elasticfilesystem:DeleteReplicationConfiguration</code>
                  action. </p>
                tags:
                  - Delete
                  - Replication
                  - Configurations
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
            /2015-02-01/create-tags/{FileSystemId}:
              POST:
                summary: CreateTags
                description: >-
                  <note> <p>DEPRECATED - <code>CreateTags</code> is deprecated
                  and not maintained. To create tags for EFS resources, use the
                  API action.</p> </note> <p>Creates or overwrites tags
                  associated with a file system. Each tag is a key-value pair.
                  If a tag key specified in the request already exists on the
                  file system, this operation overwrites its value with the
                  value provided in the request. If you add the
                  <code>Name</code> tag to your file system, Amazon EFS returns
                  it in the response to the <a>DescribeFileSystems</a>
                  operation. </p> <p>This operation requires permission for the
                  <code>elasticfilesystem:CreateTags</code> action.</p>
                tags:
                  - Create
                  - Tags
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
            /2015-02-01/access-points/{AccessPointId}:
              DELETE:
                summary: DeleteAccessPoint
                description: >-
                  <p>Deletes the specified access point. After deletion is
                  complete, new clients can no longer connect to the access
                  points. Clients connected to the access point at the time of
                  deletion will continue to function until they terminate their
                  connection.</p> <p>This operation requires permissions for the
                  <code>elasticfilesystem:DeleteAccessPoint</code> action.</p>
                tags:
                  - Delete
                  - Access
                  - Points
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
            /2015-02-01/file-systems/{FileSystemId}:
              PUT:
                summary: UpdateFileSystem
                description: >-
                  <p>Updates the throughput mode or the amount of provisioned
                  throughput of an existing file system.</p>
                tags:
                  - Update
                  - File
                  - Systems
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
            /2015-02-01/file-systems/{FileSystemId}/policy:
              PUT:
                summary: PutFileSystemPolicy
                description: >-
                  <p>Applies an Amazon EFS <code>FileSystemPolicy</code> to an
                  Amazon EFS file system. A file system policy is an IAM
                  resource-based policy and can contain multiple policy
                  statements. A file system always has exactly one file system
                  policy, which can be the default policy or an explicit policy
                  set or updated using this API operation. EFS file system
                  policies have a 20,000 character limit. When an explicit
                  policy is set, it overrides the default policy. For more
                  information about the default file system policy, see <a
                  href="https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html#default-filesystempolicy">Default
                  EFS File System Policy</a>. </p> <note> <p>EFS file system
                  policies have a 20,000 character limit.</p> </note> <p>This
                  operation requires permissions for the
                  <code>elasticfilesystem:PutFileSystemPolicy</code> action.</p>
                tags:
                  - Put
                  - File
                  - Systems
                  - Policies
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
            /2015-02-01/mount-targets/{MountTargetId}:
              DELETE:
                summary: DeleteMountTarget
                description: >-
                  <p>Deletes the specified mount target.</p> <p>This operation
                  forcibly breaks any mounts of the file system by using the
                  mount target that is being deleted, which might disrupt
                  instances or applications using those mounts. To avoid
                  applications getting cut off abruptly, you might consider
                  unmounting any mounts of the mount target, if feasible. The
                  operation also deletes the associated network interface.
                  Uncommitted writes might be lost, but breaking a mount target
                  using this operation does not corrupt the file system itself.
                  The file system you created remains. You can mount an EC2
                  instance in your VPC by using another mount target.</p>
                  <p>This operation requires permissions for the following
                  action on the file system:</p> <ul> <li> <p>
                  <code>elasticfilesystem:DeleteMountTarget</code> </p> </li>
                  </ul> <note> <p>The <code>DeleteMountTarget</code> call
                  returns while the mount target state is still
                  <code>deleting</code>. You can check the mount target deletion
                  by calling the <a>DescribeMountTargets</a> operation, which
                  returns a list of mount target descriptions for the given file
                  system. </p> </note> <p>The operation also requires
                  permissions for the following Amazon EC2 action on the mount
                  target's network interface:</p> <ul> <li> <p>
                  <code>ec2:DeleteNetworkInterface</code> </p> </li> </ul>
                tags:
                  - Delete
                  - Mount
                  - Target
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
            /2015-02-01/delete-tags/{FileSystemId}:
              POST:
                summary: DeleteTags
                description: >-
                  <note> <p>DEPRECATED - <code>DeleteTags</code> is deprecated
                  and not maintained. To remove tags from EFS resources, use the
                  API action.</p> </note> <p>Deletes the specified tags from a
                  file system. If the <code>DeleteTags</code> request includes a
                  tag key that doesn't exist, Amazon EFS ignores it and doesn't
                  cause an error. For more information about tags and related
                  restrictions, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Tag
                  restrictions</a> in the <i>Billing and Cost Management User
                  Guide</i>.</p> <p>This operation requires permissions for the
                  <code>elasticfilesystem:DeleteTags</code> action.</p>
                tags:
                  - Delete
                  - Tags
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
            /2015-02-01/account-preferences:
              PUT:
                summary: PutAccountPreferences
                description: >-
                  <p>Use this operation to set the account preference in the
                  current Amazon Web Services Region to use long 17 character
                  (63 bit) or short 8 character (32 bit) resource IDs for new
                  EFS file system and mount target resources. All existing
                  resource IDs are not affected by any changes you make. You can
                  set the ID preference during the opt-in period as EFS
                  transitions to long resource IDs. For more information, see <a
                  href="https://docs.aws.amazon.com/efs/latest/ug/manage-efs-resource-ids.html">Managing
                  Amazon EFS resource IDs</a>.</p> <note> <p>Starting in
                  October, 2021, you will receive an error if you try to set the
                  account preference to use the short 8 character format
                  resource ID. Contact Amazon Web Services support if you
                  receive an error and must use short IDs for file system and
                  mount target resources.</p> </note>
                tags:
                  - Put
                  - Account
                  - Preferences
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
            /2015-02-01/file-systems/{FileSystemId}/backup-policy:
              PUT:
                summary: PutBackupPolicy
                description: >-
                  <p>Updates the file system's backup policy. Use this action to
                  start or stop automatic backups of the file system. </p>
                tags:
                  - Put
                  - Backup
                  - Policies
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
            /2015-02-01/file-systems/{FileSystemId}/lifecycle-configuration:
              PUT:
                summary: PutLifecycleConfiguration
                description: >-
                  <p>Use this action to manage storage for your file system. A
                  <code>LifecycleConfiguration</code> consists of one or more
                  <code>LifecyclePolicy</code> objects that define the
                  following:</p> <ul> <li> <p> <b> <code>TransitionToIA</code>
                  </b> – When to move files in the file system from primary
                  storage (Standard storage class) into the Infrequent Access
                  (IA) storage.</p> </li> <li> <p> <b>
                  <code>TransitionToArchive</code> </b> – When to move files in
                  the file system from their current storage class (either IA or
                  Standard storage) into the Archive storage.</p> <p>File
                  systems cannot transition into Archive storage before
                  transitioning into IA storage. Therefore, TransitionToArchive
                  must either not be set or must be later than
                  TransitionToIA.</p> <note> <p> The Archive storage class is
                  available only for file systems that use the Elastic
                  Throughput mode and the General Purpose Performance mode. </p>
                  </note> </li> </ul> <ul> <li> <p> <b>
                  <code>TransitionToPrimaryStorageClass</code> </b> – Whether to
                  move files in the file system back to primary storage
                  (Standard storage class) after they are accessed in IA or
                  Archive storage.</p> </li> </ul> <p>For more information, see
                  <a
                  href="https://docs.aws.amazon.com/efs/latest/ug/lifecycle-management-efs.html">
                  Managing file system storage</a>.</p> <p>Each Amazon EFS file
                  system supports one lifecycle configuration, which applies to
                  all files in the file system. If a
                  <code>LifecycleConfiguration</code> object already exists for
                  the specified file system, a
                  <code>PutLifecycleConfiguration</code> call modifies the
                  existing configuration. A
                  <code>PutLifecycleConfiguration</code> call with an empty
                  <code>LifecyclePolicies</code> array in the request body
                  deletes any existing <code>LifecycleConfiguration</code>. In
                  the request, specify the following: </p> <ul> <li> <p>The ID
                  for the file system for which you are enabling, disabling, or
                  modifying Lifecycle management.</p> </li> <li> <p>A
                  <code>LifecyclePolicies</code> array of
                  <code>LifecyclePolicy</code> objects that define when to move
                  files to IA storage, to Archive storage, and back to primary
                  storage.</p> <note> <p>Amazon EFS requires that each
                  <code>LifecyclePolicy</code> object have only have a single
                  transition, so the <code>LifecyclePolicies</code> array needs
                  to be structured with separate <code>LifecyclePolicy</code>
                  objects. See the example requests in the following section for
                  more information.</p> </note> </li> </ul> <p>This operation
                  requires permissions for the
                  <code>elasticfilesystem:PutLifecycleConfiguration</code>
                  operation.</p> <p>To apply a
                  <code>LifecycleConfiguration</code> object to an encrypted
                  file system, you need the same Key Management Service
                  permissions as when you created the encrypted file system.</p>
                tags:
                  - Put
                  - Lifecycle
                  - Configurations
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
                  - Lifecycle
            /2015-02-01/mount-targets/{MountTargetId}/security-groups:
              PUT:
                summary: ModifyMountTargetSecurityGroups
                description: >-
                  <p>Modifies the set of security groups in effect for a mount
                  target.</p> <p>When you create a mount target, Amazon EFS also
                  creates a new network interface. For more information, see
                  <a>CreateMountTarget</a>. This operation replaces the security
                  groups in effect for the network interface associated with a
                  mount target, with the <code>SecurityGroups</code> provided in
                  the request. This operation requires that the network
                  interface of the mount target has been created and the
                  lifecycle state of the mount target is not
                  <code>deleted</code>. </p> <p>The operation requires
                  permissions for the following actions:</p> <ul> <li> <p>
                  <code>elasticfilesystem:ModifyMountTargetSecurityGroups</code>
                  action on the mount target's file system. </p> </li> <li> <p>
                  <code>ec2:ModifyNetworkInterfaceAttribute</code> action on the
                  mount target's network interface. </p> </li> </ul>
                tags:
                  - Modify
                  - Mount
                  - Target
                  - Security
                  - Groups
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
                  - Lifecycle
                  - Security
                  - Groups
            /2015-02-01/file-systems/replication-configurations:
              GET:
                summary: DescribeReplicationConfigurations
                description: >-
                  <p>Retrieves the replication configuration for a specific file
                  system. If a file system is not specified, all of the
                  replication configurations for the Amazon Web Services account
                  in an Amazon Web Services Region are retrieved.</p>
                tags:
                  - Describe
                  - Replication
                  - Configurations
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
                  - Lifecycle
                  - Security
                  - Groups
                  - Configurations
            /2015-02-01/tags/{FileSystemId}/:
              GET:
                summary: DescribeTags
                description: >-
                  <note> <p>DEPRECATED - The <code>DescribeTags</code> action is
                  deprecated and not maintained. To view tags associated with
                  EFS resources, use the <code>ListTagsForResource</code> API
                  action.</p> </note> <p>Returns the tags associated with a file
                  system. The order of tags returned in the response of one
                  <code>DescribeTags</code> call and the order of tags returned
                  across the responses of a multiple-call iteration (when using
                  pagination) is unspecified. </p> <p> This operation requires
                  permissions for the
                  <code>elasticfilesystem:DescribeTags</code> action. </p>
                tags:
                  - Describe
                  - Tags
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
                  - Lifecycle
                  - Security
                  - Groups
                  - Configurations
            /2015-02-01/resource-tags/{ResourceId}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes tags from an EFS resource. You can remove tags from
                  EFS file systems and access points using this API
                  operation.</p> <p>This operation requires permissions for the
                  <code>elasticfilesystem:UntagResource</code> action.</p>
                tags:
                  - Untag
                  - Resources
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
                  - Lifecycle
                  - Security
                  - Groups
                  - Configurations
                  - Resources
            /2015-02-01/file-systems/{FileSystemId}/protection:
              PUT:
                summary: UpdateFileSystemProtection
                description: >-
                  <p>Updates protection on the file system.</p> <p>This
                  operation requires permissions for the
                  <code>elasticfilesystem:UpdateFileSystemProtection</code> ac
                tags:
                  - Update
                  - File
                  - Systems
                  - Protection
                  - '2015'
                  - '02'
                  - '01'
                  - Access
                  - Points
                  - File
                  - Systems
                  - Mount
                  - Targets
                  - Source
                  - Systems
                  - Identifiers
                  - Replication
                  - Configurations
                  - Points
                  - Policies
                  - Target
                  - Account
                  - Preferences
                  - Backup
                  - Lifecycle
                  - Security
                  - Groups
                  - Configurations
                  - Resources
                  - Protection
    overlays:
      - type: APIs.io Search
        url: overlays/elasticfilesystem-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticfilesystem-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticfilesystem
  - name: nimble
    description: >-
      <p>Welcome to the Amazon Nimble Studio API reference. This API reference
      provides methods, schema, resources, parameters, and more to help you get
      the most out of Nimble Studio.</p> <p>Nimble Studio is a virtual studio
      that empowers visual effects, animation, and interactive content teams to
      create content securely within a scalable, private cloud service.</p>
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
            title: nimble
          paths:
            /2020-08-01/studios/{studioId}/eula-acceptances:
              GET:
                summary: ListEulaAcceptances
                description: <p>List EULA acceptances.</p>
                tags:
                  - Lists
                  - EULA
                  - Acceptances
                  - Identifiers
                  - EULA
                  - Acceptances
            /2020-08-01/studios/{studioId}/launch-profiles:
              GET:
                summary: ListLaunchProfiles
                description: <p>List all the launch profiles a studio.</p>
                tags:
                  - Lists
                  - Launch
                  - Profiles
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
            /2020-08-01/studios/{studioId}/streaming-images:
              GET:
                summary: ListStreamingImages
                description: >-
                  <p>List the streaming image resources available to this
                  studio.</p> <p>This list will contain both images provided by
                  Amazon Web Services, as well as streaming images that you have
                  created in your studio.</p>
                tags:
                  - Lists
                  - Streaming
                  - Images
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
            /2020-08-01/studios/{studioId}/streaming-sessions:
              GET:
                summary: ListStreamingSessions
                description: <p>Lists the streaming sessions in a studio.</p>
                tags:
                  - Lists
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/streams:
              POST:
                summary: CreateStreamingSessionStream
                description: >-
                  <p>Creates a streaming session stream for a streaming
                  session.</p> <p>After invoking this API, invoke
                  GetStreamingSessionStream with the returned streamId to poll
                  the resource until it is in the <code>READY</code> state.</p>
                tags:
                  - Create
                  - Streaming
                  - Sessions
                  - Stream
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
            /2020-08-01/studios:
              GET:
                summary: ListStudios
                description: >-
                  <p>List studios in your Amazon Web Services accounts in the
                  requested Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Studios
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
            /2020-08-01/studios/{studioId}/studio-components:
              GET:
                summary: ListStudioComponents
                description: <p>Lists the <code>StudioComponents</code> in a studio.</p>
                tags:
                  - Lists
                  - Studios
                  - Components
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}:
              PATCH:
                summary: UpdateLaunchProfile
                description: <p>Update a launch profile.</p>
                tags:
                  - Update
                  - Launch
                  - Profiles
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/membership/{principalId}:
              PATCH:
                summary: UpdateLaunchProfileMember
                description: <p>Update a user persona in launch profile membership.</p>
                tags:
                  - Update
                  - Launch
                  - Profiles
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
            /2020-08-01/studios/{studioId}/streaming-images/{streamingImageId}:
              PATCH:
                summary: UpdateStreamingImage
                description: <p>Update streaming image.</p>
                tags:
                  - Update
                  - Streaming
                  - Images
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}:
              GET:
                summary: GetStreamingSession
                description: >-
                  <p>Gets StreamingSession resource.</p> <p>Invoke this
                  operation to poll for a streaming session state while creating
                  or deleting a session.</p>
                tags:
                  - Get
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
            /2020-08-01/studios/{studioId}:
              PATCH:
                summary: UpdateStudio
                description: >-
                  <p>Update a Studio resource.</p> <p>Currently, this operation
                  only supports updating the displayName of your studio.</p>
                tags:
                  - Update
                  - Studios
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
            /2020-08-01/studios/{studioId}/studio-components/{studioComponentId}:
              PATCH:
                summary: UpdateStudioComponent
                description: <p>Updates a studio component resource.</p>
                tags:
                  - Update
                  - Studios
                  - Components
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
            /2020-08-01/studios/{studioId}/membership/{principalId}:
              GET:
                summary: GetStudioMember
                description: <p>Get a user's membership in a studio.</p>
                tags:
                  - Get
                  - Studios
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
            /2020-08-01/eulas/{eulaId}:
              GET:
                summary: GetEula
                description: <p>Get EULA.</p>
                tags:
                  - Get
                  - EULA
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/details:
              GET:
                summary: GetLaunchProfileDetails
                description: >-
                  <p>Launch profile details include the launch profile resource
                  and summary information of resources that are used by, or
                  available to, the launch profile. This includes the name and
                  description of all studio components used by the launch
                  profiles, and the name and description of streaming images
                  that can be used with this launch profile.</p>
                tags:
                  - Get
                  - Launch
                  - Profiles
                  - Details
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/init:
              GET:
                summary: GetLaunchProfileInitialization
                description: <p>Get a launch profile initialization.</p>
                tags:
                  - Get
                  - Launch
                  - Profiles
                  - Initialization
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
            /2020-08-01/studios/{studioId}/streaming-session-backups/{backupId}:
              GET:
                summary: GetStreamingSessionBackup
                description: >-
                  <p>Gets <code>StreamingSessionBackup</code> resource.</p>
                  <p>Invoke this operation to poll for a streaming session
                  backup while stopping a streaming session.</p>
                tags:
                  - Get
                  - Streaming
                  - Sessions
                  - Backup
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/streams/{streamId}:
              GET:
                summary: GetStreamingSessionStream
                description: >-
                  <p>Gets a StreamingSessionStream for a streaming session.</p>
                  <p>Invoke this operation to poll the resource after invoking
                  <code>CreateStreamingSessionStream</code>.</p> <p>After the
                  <code>StreamingSessionStream</code> changes to the
                  <code>READY</code> state, the url property will contain a
                  stream to be used with the DCV streaming client.</p>
                tags:
                  - Get
                  - Streaming
                  - Sessions
                  - Stream
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
            /2020-08-01/eulas:
              GET:
                summary: ListEulas
                description: <p>List EULAs.</p>
                tags:
                  - Lists
                  - Eulas
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/membership:
              POST:
                summary: PutLaunchProfileMembers
                description: >-
                  <p>Add/update users with given persona to launch profile
                  membership.</p>
                tags:
                  - Put
                  - Launch
                  - Profiles
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/studios/{studioId}/streaming-session-backups:
              GET:
                summary: ListStreamingSessionBackups
                description: <p>Lists the backups of a streaming session in a studio.</p>
                tags:
                  - Lists
                  - Streaming
                  - Sessions
                  - Backups
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/studios/{studioId}/membership:
              POST:
                summary: PutStudioMembers
                description: >-
                  <p>Add/update users with given persona to studio
                  membership.</p>
                tags:
                  - Put
                  - Studios
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deletes the tags for a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/start:
              POST:
                summary: StartStreamingSession
                description: >-
                  <p>Transitions sessions from the <code>STOPPED</code> state
                  into the <code>READY</code> state. The
                  <code>START_IN_PROGRESS</code> state is the intermediate state
                  between the <code>STOPPED</code> and <code>READY</code>
                  states.</p>
                tags:
                  - Start
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
                  - Start
            /2020-08-01/studios/{studioId}/sso-configuration:
              PUT:
                summary: StartStudioSSOConfigurationRepair
                description: >-
                  <p>Repairs the IAM Identity Center configuration for a given
                  studio.</p> <p>If the studio has a valid IAM Identity Center
                  configuration currently associated with it, this operation
                  will fail with a validation error.</p> <p>If the studio does
                  not have a valid IAM Identity Center configuration currently
                  associated with it, then a new IAM Identity Center application
                  is created for the studio and the studio is changed to the
                  <code>READY</code> state.</p> <p>After the IAM Identity Center
                  application is repaired, you must use the Amazon Nimble Studio
                  console to add administrators and users to your studio.</p>
                tags:
                  - Start
                  - Studios
                  - Configurations
                  - Repair
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
                  - Start
                  - SSO
                  - Configurations
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/stop:
              POST:
                summary: StopStreamingSession
                description: >-
                  <p>Transitions sessions from the <code>READY</code> state into
                  the <code>STOPPED</code> state. The
                  <code>STOP_IN_PROGRESS</code> state is the intermediate state
                  between the <code>READY</code> and <code>STOPPED</code> s
                tags:
                  - Stop
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
                  - Start
                  - SSO
                  - Configurations
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/nimble-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/nimble-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:nimble
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---