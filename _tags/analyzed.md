---
name: Analyzed
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/analyzed.png
url: https://example.com/apis/analyzed.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Analyzed
apis:
  - name: accessanalyzer
    description: >-
      <p>Identity and Access Management Access Analyzer helps you to set,
      verify, and refine your IAM policies by providing a suite of capabilities.
      Its features include findings for external and unused access, basic and
      custom policy checks for validating policies, and policy generation to
      generate fine-grained policies. To start using IAM Access Analyzer to
      identify external or unused access, you first need to create an
      analyzer.</p> <p> <b>External access analyzers</b> help identify potential
      risks of accessing resources by enabling you to identify any resource
      policies that grant access to an external principal. It does this by using
      logic-based reasoning to analyze resource-based policies in your Amazon
      Web Services environment. An external principal can be another Amazon Web
      Services account, a root user, an IAM user or role, a federated user, an
      Amazon Web Services service, or an anonymous user. You can also use IAM
      Access Analyzer to preview public and cross-account access to your
      resources before deploying permissions changes.</p> <p> <b>Unused access
      analyzers</b> help identify potential identity access risks by enabling
      you to identify unused IAM roles, unused access keys, unused console
      passwords, and IAM principals with unused service and action-level
      permissions.</p> <p>Beyond findings, IAM Access Analyzer provides basic
      and custom policy checks to validate IAM policies before deploying
      permissions changes. You can use policy generation to refine permissions
      by attaching a policy generated using access activity logged in CloudTrail
      logs. </p> <p>This guide describes the IAM Access Analyzer operations that
      you can call programmatically. For general information about IAM Access
      Analyzer, see <a
      href="https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html">Identity
      and Access Management Access Analyzer</a> in the <b>IAM User
      Guide</b>.</p>
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
            title: accessanalyzer
          paths:
            /archive-rule:
              PUT:
                summary: Apply Archive Rule
                description: >-
                  <p>Retroactively applies the archive rule to existing findings
                  that meet the archive rule criteria.</p>
                tags:
                  - Apply
                  - Archive
                  - Rules
                  - Archive
                  - Rules
            /policy/generation/{jobId}:
              GET:
                summary: Get Generated Policy
                description: >-
                  <p>Retrieves the policy that was generated using
                  <code>StartPolicyGeneration</code>. </p>
                tags:
                  - Get
                  - Generated
                  - Policies
                  - Archive
                  - Rules
                  - Identifiers
            /policy/check-access-not-granted:
              POST:
                summary: Check Access Not Granted
                description: >-
                  <p>Checks whether the specified access isn't allowed by a
                  policy.</p>
                tags:
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
            /policy/check-no-new-access:
              POST:
                summary: Check No New Access
                description: >-
                  <p>Checks whether new access is allowed for an updated policy
                  when compared to the existing policy.</p> <p>You can find
                  examples for reference policies and learn how to set up and
                  run a custom policy check for new access in the <a
                  href="https://github.com/aws-samples/iam-access-analyzer-custom-policy-check-samples">IAM
                  Access Analyzer custom policy checks samples</a> repository on
                  GitHub. The reference policies in this repository are meant to
                  be passed to the <code>existingPolicyDocument</code> request
                  parameter.</p>
                tags:
                  - Checks
                  - 'No'
                  - New
                  - Access
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
            /access-preview:
              GET:
                summary: ListAccessPreviews
                description: >-
                  <p>Retrieves a list of access previews for the specified
                  analyzer.</p>
                tags:
                  - Lists
                  - Access
                  - Previews
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
            /analyzer:
              GET:
                summary: ListAnalyzers
                description: <p>Retrieves a list of analyzers.</p>
                tags:
                  - Lists
                  - Analyzers
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
            /analyzer/{analyzerName}/archive-rule:
              GET:
                summary: ListArchiveRules
                description: >-
                  <p>Retrieves a list of archive rules created for the specified
                  analyzer.</p>
                tags:
                  - Lists
                  - Archive
                  - Rules
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /analyzer/{analyzerName}:
              GET:
                summary: GetAnalyzer
                description: <p>Retrieves information about the specified analyzer.</p>
                tags:
                  - Get
                  - Analyzer
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /analyzer/{analyzerName}/archive-rule/{ruleName}:
              PUT:
                summary: UpdateArchiveRule
                description: >-
                  <p>Updates the criteria and values for the specified archive
                  rule.</p>
                tags:
                  - Update
                  - Archive
                  - Rules
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /access-preview/{accessPreviewId}:
              POST:
                summary: ListAccessPreviewFindings
                description: >-
                  <p>Retrieves a list of access preview findings generated by
                  the specified access preview.</p>
                tags:
                  - Lists
                  - Access
                  - Preview
                  - Findings
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /analyzed-resource:
              POST:
                summary: ListAnalyzedResources
                description: >-
                  <p>Retrieves a list of resources of the specified type that
                  have been analyzed by the specified analyzer..</p>
                tags:
                  - Lists
                  - Analyzed
                  - Resources
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
            /finding/{id}:
              GET:
                summary: GetFinding
                description: <p>Retrieves information about the specified finding.</p>
                tags:
                  - Get
                  - Findings
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
            /findingv2/{id}:
              GET:
                summary: GetFindingV2
                description: <p>Retrieves information about the specified finding.</p>
                tags:
                  - Get
                  - Findings
                  - V2
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
            /finding:
              PUT:
                summary: UpdateFindings
                description: <p>Updates the status for the specified findings.</p>
                tags:
                  - Update
                  - Findings
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
            /findingv2:
              POST:
                summary: ListFindingsV2
                description: >-
                  <p>Retrieves a list of findings generated by the specified
                  analyzer.</p> <p>To learn about filter keys that you can use
                  to retrieve a list of findings, see <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/access-analyzer-reference-filter-keys.html">IAM
                  Access Analyzer filter keys</a> in the <b>IAM User
                  Guide</b>.</p>
                tags:
                  - Lists
                  - Findings
                  - V2
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
            /policy/generation:
              PUT:
                summary: StartPolicyGeneration
                description: <p>Starts the policy generation request.</p>
                tags:
                  - Start
                  - Policies
                  - Generation
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
                  - ARN
            /resource/scan:
              POST:
                summary: StartResourceScan
                description: >-
                  <p>Immediately starts a scan of the policies applied to the
                  specified resource.</p>
                tags:
                  - Start
                  - Resources
                  - Scans
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
                  - ARN
                  - Scans
            /policy/validation:
              POST:
                summary: ValidatePolicy
                description: >-
                  <p>Requests the validation of a policy and returns a list of
                  findings. The findings help you identify issues and provide
                  actionable recommendations to resolve the issue and enable you
                  to author functional policies that meet security best pract
                tags:
                  - Validate
                  - Policies
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
                  - ARN
                  - Scans
                  - Validations
    overlays:
      - type: APIs.io Search
        url: overlays/accessanalyzer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/accessanalyzer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:accessanalyzer
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---