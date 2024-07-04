---
name: Anchors
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anchors.png
url: https://example.com/apis/anchors.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anchors
apis:
  - name: rolesanywhere
    description: >-
      <p>Identity and Access Management Roles Anywhere provides a secure way for
      your workloads such as servers, containers, and applications that run
      outside of Amazon Web Services to obtain temporary Amazon Web Services
      credentials. Your workloads can use the same IAM policies and roles you
      have for native Amazon Web Services applications to access Amazon Web
      Services resources. Using IAM Roles Anywhere eliminates the need to manage
      long-term credentials for workloads running outside of Amazon Web
      Services.</p> <p> To use IAM Roles Anywhere, your workloads must use X.509
      certificates issued by their certificate authority (CA). You register the
      CA with IAM Roles Anywhere as a trust anchor to establish trust between
      your public key infrastructure (PKI) and IAM Roles Anywhere. If you don't
      manage your own PKI system, you can use Private Certificate Authority to
      create a CA and then use that to establish trust with IAM Roles Anywhere.
      </p> <p>This guide describes the IAM Roles Anywhere operations that you
      can call programmatically. For more information about IAM Roles Anywhere,
      see the <a
      href="https://docs.aws.amazon.com/rolesanywhere/latest/userguide/introduction.html">IAM
      Roles Anywhere User Guide</a>.</p>
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
            title: rolesanywhere
          paths:
            /profiles:
              GET:
                summary: ListProfiles
                description: >-
                  <p>Lists all profiles in the authenticated account and Amazon
                  Web Services Region.</p> <p> <b>Required permissions: </b>
                  <code>rolesanywhere:ListProfiles</code>. </p>
                tags:
                  - Lists
                  - Profiles
                  - Profiles
            /trustanchors:
              GET:
                summary: ListTrustAnchors
                description: >-
                  <p>Lists the trust anchors in the authenticated account and
                  Amazon Web Services Region.</p> <p> <b>Required permissions:
                  </b> <code>rolesanywhere:ListTrustAnchors</code>. </p>
                tags:
                  - Lists
                  - Trust
                  - Anchors
                  - Profiles
                  - Trust Anchors
            /crl/{crlId}:
              PATCH:
                summary: UpdateCrl
                description: >-
                  <p>Updates the certificate revocation list (CRL). A CRL is a
                  list of certificates that have been revoked by the issuing
                  certificate authority (CA). IAM Roles Anywhere validates
                  against the CRL before issuing credentials.</p> <p>
                  <b>Required permissions: </b>
                  <code>rolesanywhere:UpdateCrl</code>. </p>
                tags:
                  - Update
                  - Crl
                  - Profiles
                  - Trust Anchors
                  - Identifiers
            /profile/{profileId}:
              PATCH:
                summary: UpdateProfile
                description: >-
                  <p>Updates a <i>profile</i>, a list of the roles that IAM
                  Roles Anywhere service is trusted to assume. You use profiles
                  to intersect permissions with IAM managed policies.</p> <p>
                  <b>Required permissions: </b>
                  <code>rolesanywhere:UpdateProfile</code>. </p>
                tags:
                  - Update
                  - Profiles
                  - Profiles
                  - Trust Anchors
                  - Identifiers
            /trustanchor/{trustAnchorId}:
              PATCH:
                summary: UpdateTrustAnchor
                description: >-
                  <p>Updates a trust anchor. You establish trust between IAM
                  Roles Anywhere and your certificate authority (CA) by
                  configuring a trust anchor. You can define a trust anchor as a
                  reference to an Private Certificate Authority (Private CA) or
                  by uploading a CA certificate. Your Amazon Web Services
                  workloads can authenticate with the trust anchor using
                  certificates issued by the CA in exchange for temporary Amazon
                  Web Services credentials.</p> <p> <b>Required permissions:
                  </b> <code>rolesanywhere:UpdateTrustAnchor</code>. </p>
                tags:
                  - Update
                  - Trust
                  - Anchor
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
            /crl/{crlId}/disable:
              POST:
                summary: DisableCrl
                description: >-
                  <p>Disables a certificate revocation list (CRL).</p> <p>
                  <b>Required permissions: </b>
                  <code>rolesanywhere:DisableCrl</code>. </p>
                tags:
                  - Disable
                  - Crl
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
            /profile/{profileId}/disable:
              POST:
                summary: DisableProfile
                description: >-
                  <p>Disables a profile. When disabled, temporary credential
                  requests with this profile fail.</p> <p> <b>Required
                  permissions: </b> <code>rolesanywhere:DisableProfile</code>.
                  </p>
                tags:
                  - Disable
                  - Profiles
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
            /trustanchor/{trustAnchorId}/disable:
              POST:
                summary: DisableTrustAnchor
                description: >-
                  <p>Disables a trust anchor. When disabled, temporary
                  credential requests specifying this trust anchor are
                  unauthorized.</p> <p> <b>Required permissions: </b>
                  <code>rolesanywhere:DisableTrustAnchor</code>. </p>
                tags:
                  - Disable
                  - Trust
                  - Anchor
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
            /crl/{crlId}/enable:
              POST:
                summary: EnableCrl
                description: >-
                  <p>Enables a certificate revocation list (CRL). When enabled,
                  certificates stored in the CRL are unauthorized to receive
                  session credentials.</p> <p> <b>Required permissions: </b>
                  <code>rolesanywhere:EnableCrl</code>. </p>
                tags:
                  - Enable
                  - Crl
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
            /profile/{profileId}/enable:
              POST:
                summary: EnableProfile
                description: >-
                  <p>Enables temporary credential requests for a profile. </p>
                  <p> <b>Required permissions: </b>
                  <code>rolesanywhere:EnableProfile</code>. </p>
                tags:
                  - Enable
                  - Profiles
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
            /trustanchor/{trustAnchorId}/enable:
              POST:
                summary: EnableTrustAnchor
                description: >-
                  <p>Enables a trust anchor. When enabled, certificates in the
                  trust anchor chain are authorized for trust validation. </p>
                  <p> <b>Required permissions: </b>
                  <code>rolesanywhere:EnableTrustAnchor</code>. </p>
                tags:
                  - Enable
                  - Trust
                  - Anchor
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
            /subject/{subjectId}:
              GET:
                summary: GetSubject
                description: >-
                  <p>Gets a <i>subject</i>, which associates a certificate
                  identity with authentication attempts. The subject stores
                  auditing information such as the status of the last
                  authentication attempt, the certificate data used in the
                  attempt, and the last time the associated identity attempted
                  authentication. </p> <p> <b>Required permissions: </b>
                  <code>rolesanywhere:GetSubject</code>. </p>
                tags:
                  - Get
                  - Subjects
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
            /crls:
              GET:
                summary: ListCrls
                description: >-
                  <p>Lists all certificate revocation lists (CRL) in the
                  authenticated account and Amazon Web Services Region.</p> <p>
                  <b>Required permissions: </b>
                  <code>rolesanywhere:ListCrls</code>. </p>
                tags:
                  - Lists
                  - Crls
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
            /subjects:
              GET:
                summary: ListSubjects
                description: >-
                  <p>Lists the subjects in the authenticated account and Amazon
                  Web Services Region.</p> <p> <b>Required permissions: </b>
                  <code>rolesanywhere:ListSubjects</code>. </p>
                tags:
                  - Lists
                  - Subjects
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
                  - Subjects
            /ListTagsForResource:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags attached to the resource.</p> <p>
                  <b>Required permissions: </b>
                  <code>rolesanywhere:ListTagsForResource</code>. </p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
                  - Subjects
                  - Lists
                  - Tags
                  - For
                  - Resources
            /put-notifications-settings:
              PATCH:
                summary: PutNotificationSettings
                description: >-
                  <p>Attaches a list of <i>notification settings</i> to a trust
                  anchor.</p> <p>A notification setting includes information
                  such as event name, threshold, status of the notification
                  setting, and the channel to notify.</p> <p> <b>Required
                  permissions: </b>
                  <code>rolesanywhere:PutNotificationSettings</code>. </p>
                tags:
                  - Put
                  - Notifications
                  - Settings
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
                  - Subjects
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Put
                  - Notifications
                  - Settings
            /reset-notifications-settings:
              PATCH:
                summary: ResetNotificationSettings
                description: >-
                  <p>Resets the <i>custom notification setting</i> to IAM Roles
                  Anywhere default setting. </p> <p> <b>Required permissions:
                  </b> <code>rolesanywhere:ResetNotificationSettings</code>.
                  </p>
                tags:
                  - Reset
                  - Notifications
                  - Settings
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
                  - Subjects
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Put
                  - Notifications
                  - Settings
                  - Reset
            /TagResource:
              POST:
                summary: TagResource
                description: >-
                  <p>Attaches tags to a resource.</p> <p> <b>Required
                  permissions: </b> <code>rolesanywhere:TagResource</code>. </p>
                tags:
                  - Tags
                  - Resources
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
                  - Subjects
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Put
                  - Notifications
                  - Settings
                  - Reset
                  - Tags
            /UntagResource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes tags from the resource.</p> <p> <b>Required
                  permissions: </b> <code>rolesanywhere:UntagResource</c
                tags:
                  - Untag
                  - Resources
                  - Profiles
                  - Trust Anchors
                  - Identifiers
                  - Anchor
                  - Disable
                  - Enable
                  - Crls
                  - Subjects
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Put
                  - Notifications
                  - Settings
                  - Reset
                  - Tags
                  - Unt
    overlays:
      - type: APIs.io Search
        url: overlays/rolesanywhere-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rolesanywhere-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rolesanywhere
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---