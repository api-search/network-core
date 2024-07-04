---
name: Coverage
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/coverage.png
url: https://example.com/apis/coverage.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Coverage
apis:
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
                  - Members
                  - Publishing
                  - Destinations
                  - Create
                  - null
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
                  - null
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
                  - null
            /cis/scan-configuration/create:
              POST:
                summary: CreateCisScanConfiguration
                description: <p>Creates a CIS scan configuration.</p>
                tags:
                  - Create
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
                  - null
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
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/inspector2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/inspector2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:inspector2
  - name: FactSet Documents Distributor - CallStreet Events
    description: >-
      CallStreet Events contains all the Documents Distributor APIs that offer
      events data such as Events Audio and Near Real-Time Transcripts.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/documents-distributor-callstreet-events
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Documents Distributor - CallStreet Events
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: >-
              https://developer.factset.com/api-catalog/documents-distributor-callstreet-events
          paths:
            /docs-distributor/audio/v1/history-files:
              get:
                summary: >-
                  Retrieve historical audio recordings and related metadata
                  within FactSet coverage.
                tags:
                  - Retrieve
                  - Historical
                  - Audio
                  - Recordings
                  - And
                  - Related
                  - Metadata
                  - Within
                  - Fact
                  - Set
                  - Coverage.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                description: >

                  * Returns the **untrimmed** historical audio recordings and
                  related metadata dating back from May 10, 2011 to Sep 30,
                  2022.


                  * Returns the **trimmed** historical audio recordings and
                  related metadata dating back from May 10, 2011 to Dec 31,
                  2022.




                  Query parameters can be used to filter and narrow down the
                  results.
            /docs-distributor/audio/v1/list-files:
              get:
                summary: >-
                  Retrieve latest audio recordings and related metadata within
                  FactSet coverage.
                tags:
                  - Retrieve
                  - Latest
                  - Audio
                  - Recordings
                  - And
                  - Related
                  - Metadata
                  - Within
                  - Fact
                  - Set
                  - Coverage.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                description: >-
                  Returns the latest audio recordings. Query parameters can be
                  used to filter and narrow down the results.
            /bulk-documents/nrt/v1/calls:
              get:
                summary: Returns the active calls happening at the moment.
                tags:
                  - Returns
                  - The
                  - Active
                  - Calls
                  - Happening
                  - At
                  - Moment.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                description: Returns the active calls happening at the moment
            /bulk-documents/nrt/v1/list-snippets:
              get:
                summary: Returns the latest transcript snippets from an active call.
                tags:
                  - Returns
                  - The
                  - Latest
                  - Transcript
                  - Snippets
                  - From
                  - An
                  - Active
                  - Call.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                  - Snippets
                description: Returns the latest snippets from an active call
            /bulk-documents/nrt/v1/speakerids:
              get:
                summary: >-
                  Returns the latest speakerIds with the confidence scores
                  generated for an active call.
                tags:
                  - Returns
                  - The
                  - Latest
                  - Speaker
                  - Ids
                  - With
                  - Confidence
                  - Scores
                  - Generated
                  - For
                  - An
                  - Active
                  - Call.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                  - Snippets
                  - Speakerids
                description: >-
                  Returns the latest speakerIds with the cosine
                  scores(confidence scores) generated for an active call.
            /bulk-documents/nrt/v1/indexed-nrt:
              get:
                summary: >-
                  Returns the  indexed transcript data  in small increments
                  throughout the duration of an active call.
                tags:
                  - Returns
                  - The
                  - Indexed
                  - Transcript
                  - Data
                  - In
                  - Small
                  - Increments
                  - Throughout
                  - Duration
                  - Of
                  - An
                  - Active
                  - Call.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                  - Snippets
                  - Speakerids
                  - Indexed
                description: >-
                  Returns the  indexed transcript data  in small increments
                  throughout the duration of an active call.
          tags:
            - name: Events Audio
              description: >-
                The Events Audio API provides access to historical as well as
                the latest audio recordings of various company events covered by
                FactSet.
            - name: Near Real-Time Transcripts
              description: >-
                The Near Real-Time Transcripts API enables access to Near
                Real-time Transcripts provided by CallStreet to tim
    overlays:
      - type: APIs.io Search
        url: overlays/documents-distributor-callstreet-events-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/documents-distributor-callstreet-events-openapi-api-evangelist-ratings.yml
    aid: factset:factset-documents-distributor-callstreet-events
  - name: FactSet Tick History API
    description: >-
      Tick History provides dynamic access to historical tick data for a
      specific security for specific dates or date range.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-tick-history-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Tick History
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/factset-tick-history-api
          paths:
            /level1/coverage:
              get:
                tags:
                  - Returns
                  - The
                  - Coverage
                  - For
                  - Requested
                  - Ticker/isin
                  - Along
                  - With
                  - Other
                  - Response
                  - Fields
                  - Level1
                  - Data.
                  - Level1
                  - Coverage
                summary: >-
                  Returns the coverage for the requested ticker/isin along with
                  other response fields for Level1 data.
                description: Returns coverage for specified tickers for Level1 Data
            /level1/files/create:
              post:
                tags:
                  - Requests
                  - The
                  - Creation
                  - Of
                  - Tick-by-tick
                  - File
                  - Level1
                  - Coverage
                  - Files
                  - Create
                summary: Requests the creation of tick-by-tick file
                description: Data available from 20120101 to previous day.
            /level1/files/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - Of
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                summary: Returns the status of the ID
                description: >-
                  Need to plug-in the id get from /create endpoint into /status
                  endpoint
            /level1/files/get:
              get:
                tags:
                  - Returns
                  - The
                  - Tick-by-tick
                  - Data
                  - In
                  - Files
                  - Requested
                  - /create
                  - Endpoint
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                summary: >-
                  Returns the tick-by-tick data in files requested in the
                  /create endpoint
                description: Returns the files from tickhistory endpoint
            /level1/files/minute-bars/create:
              post:
                tags:
                  - Requests
                  - The
                  - Creation
                  - Of
                  - Minute
                  - Bars
                  - File
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                summary: Requests the creation of Minute bars file
                description: >-
                  1-minute bars available from 20120101 to previous day. Per
                  request able to fetch upto 6 months of data.
            /level1/files/minute-bars/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - Of
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                summary: Returns the status of the ID
                description: >-
                  Need to plug-in the id get from /create endpoint into /status
                  endpoint
            /level1/files/minute-bars/get:
              get:
                tags:
                  - Returns
                  - The
                  - Minute
                  - Bars
                  - Data
                  - In
                  - Files
                  - Requested
                  - /create
                  - Endpoint
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                summary: >-
                  Returns the Minute bars data in files requested in the /create
                  endpoint
                description: Returns the files from tickhistory endpoint
            /level2/files/create:
              post:
                tags:
                  - Returns
                  - The
                  - For
                  - Requested
                  - Data.
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                  - Level2
                summary: Returns the ID for the requested data.
                description: Data available from past 6 years to previous day.
            /level2/files/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - Of
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                  - Level2
                summary: Returns the status of the ID
                description: >-
                  Need to plug-in the id get from /create endpoint into /status
                  endpoint
            /level2/files/get:
              get:
                tags:
                  - Returns
                  - The
                  - Tick
                  - History
                  - Files
                  - Requested
                  - In
                  - /create
                  - Endpoint
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                  - Level2
                summary: >-
                  Returns the tick history files requested in the /create
                  endpoint
                description: Returns the files from tickhistory endpoint
          tags:
            - name: Level 1
              description: >-
                API provides access to check coverage and retrieve Level 1
                historical tick data
            - name: Level 2
              description: API provides access to the  historical tick data up
    overlays:
      - type: APIs.io Search
        url: overlays/tick-history-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/tick-history-openapi-api-evangelist-ratings.yml
    aid: factset:factset-tick-history-api
  - name: FactSet Global Filings API
    description: ' This API is designed to expose document search and document retrieval functionality'
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/global-filings-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/global-filings-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/global-filings-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/global-filings-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/global-filings-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/global-filings-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Global Filings API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/global-filings-api
          paths:
            /search:
              get:
                summary: >-
                  Returns the filings documents and related metadata within
                  FactSet coverage.
                tags:
                  - Returns
                  - The
                  - Filings
                  - Documents
                  - And
                  - Related
                  - Metadata
                  - Within
                  - Fact
                  - Set
                  - Coverage.
                  - Search
                description: >-
                  Returns the filings documents within FactSet coverage along
                  with other response fields
            /helper:
              get:
                tags:
                  - Returns
                  - The
                  - Static
                  - Values
                  - For
                  - Various
                  - Parameters
                  - Search
                  - Helper
                summary: Returns the static values for various parameters
                description: >-
                  Returns the static values for
                  sources,formTypes,timeZones,categories based on the specified
                  parameter
            /count:
              get:
                tags:
                  - Returns
                  - The
                  - Count
                  - Of
                  - Filings
                  - For
                  - Specified
                  - Source
                  - Search
                  - Helper
                  - Count
                summary: Returns the count of filings for specified source
                description: >-
                  Returns the count of filings documents along with other
                  response fields.
          tags:
            - name: Filings API
              description: API provides access to search and download filings documents
    overlays:
      - type: APIs.io Search
        url: overlays/global-filings-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/global-filings-openapi-api-evangelist-ratings.yml
    aid: factset:factset-global-filings-api
  - name: FactSet Documents Distributor - Documents API
    description: >-
      Documents APIs that provide filings such as Global Filings and XML files
      such as StreetAccount
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/documents-distributor-documents-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-documents-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-documents-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-documents-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-documents-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-documents-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Documents Distributor - Documents API
          paths:
            /global-filings/v1/list-files:
              get:
                tags:
                  - Retrieve
                  - Filings
                  - Within
                  - Fact
                  - Set
                  - Coverage
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                summary: Retrieve filings within FactSet coverage
                description: Parameters can be used to get the filings
            /asynch/streetaccount/v1/request-files:
              get:
                tags:
                  - Returns
                  - The
                  - Job
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                  - Asynch
                  - Streetaccount
                  - Request
                summary: Returns the jobID
                description: >-
                  Give the startDate and endDate parameters as request
                  parameters in the /request-files endpoint, it returns the
                  jobID. startDate and endDate should be in YYYY-MM-DDTHH:MM:SSZ
                  format


                  This API only supports adhoc requests to retrieve historical
                  files and does not support real-time       files and if you
                  interested in require real-time push should consider the other
                  three methods         (pushed via SFTP, to QNT account, or
                  your Azure Storage). Per API request able to query till 2
                  years of data
            /asynch/streetaccount/v1/check-status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - And
                  - Percent
                  - Done
                  - Of
                  - Requested
                  - Job
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                  - Asynch
                  - Streetaccount
                  - Request
                  - Check
                  - Status
                summary: Returns the status and percentDone of the requested jobID
                description: >-
                  Need to plug-in the jobID got from /request-files into
                  /check-status endpoint
            /asynch/streetaccount/v1/get-files:
              get:
                tags:
                  - Returns
                  - The
                  - Files
                  - For
                  - Specified
                  - Daterange
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                  - Asynch
                  - Streetaccount
                  - Request
                  - Check
                  - Status
                  - Get
                summary: Returns the SA XML files for the specified daterange
                description: >-
                  Need to plug-in the jobID got from /request-files into
                  /check-status endpoint
            /asynch/news/v1/request-files:
              get:
                tags:
                  - Returns
                  - The
                  - Job
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                  - Asynch
                  - Streetaccount
                  - Request
                  - Check
                  - Status
                  - Get
                  - News
                summary: Returns the jobID
                description: >-
                  Give the startDate,endDate and source parameters as request
                  parameters in the /request-files endpoint, it returns the
                  jobID. startDate and endDate should be in YYYY-MM-DDTHH:MM:SSZ
                  format

                  This API only supports adhoc requests to retrieve historical
                  files
            /asynch/news/v1/check-status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - And
                  - Percent
                  - Done
                  - Of
                  - Requested
                  - Job
                  - Source
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                  - Asynch
                  - Streetaccount
                  - Request
                  - Check
                  - Status
                  - Get
                  - News
                summary: >-
                  Returns the status and percentDone of the requested jobID and
                  source
                description: >-
                  Need to plug-in the jobID got from /request-files into
                  /check-status endpoint
            /asynch/news/v1/get-files:
              get:
                tags:
                  - Returns
                  - The
                  - News
                  - Filings
                  - For
                  - Specified
                  - Daterange
                  - And
                  - Source
                  - Global
                  - Filings
                  - V1
                  - List
                  - Files
                  - Asynch
                  - Streetaccount
                  - Request
                  - Check
                  - Status
                  - Get
                  - News
                summary: >-
                  Returns the news filings for the specified daterange and
                  source
                description: >-
                  Need to plug-in the source and jobID got from /request-files
                  into
    overlays:
      - type: APIs.io Search
        url: overlays/documents-distributor-documents-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/documents-distributor-documents-openapi-api-evangelist-ratings.yml
    aid: factset:factset-documents-distributor-documents-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---