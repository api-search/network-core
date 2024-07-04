---
name: Compatible
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/compatible.png
url: https://example.com/apis/compatible.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Compatible
apis:
  - name: es
    description: >-
      <fullname>Amazon Elasticsearch Configuration Service</fullname> <p>Use the
      Amazon Elasticsearch Configuration API to create, configure, and manage
      Elasticsearch domains.</p> <p>For sample code that uses the Configuration
      API, see the <a
      href="https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-samples.html">Amazon
      Elasticsearch Service Developer Guide</a>. The guide also contains <a
      href="https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-request-signing.html">sample
      code for sending signed HTTP requests to the Elasticsearch APIs</a>.</p>
      <p>The endpoint for configuration service requests is region-specific:
      es.<i>region</i>.amazonaws.com. For example, es.us-east-1.amazonaws.com.
      For a current list of supported regions and endpoints, see <a
      href="http://docs.aws.amazon.com/general/latest/gr/rande.html#elasticsearch-service-regions"
      target="_blank">Regions and Endpoints</a>.</p>
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
            title: es
          paths:
            /2015-01-01/es/ccs/inboundConnection/{ConnectionId}/accept:
              PUT:
                summary: AcceptInboundCrossClusterSearchConnection
                description: >-
                  <p>Allows the destination domain owner to accept an inbound
                  cross-cluster search connection request.</p>
                tags:
                  - Accept
                  - Inbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
            /2015-01-01/tags:
              POST:
                summary: AddTags
                description: >-
                  <p>Attaches tags to an existing Elasticsearch domain. Tags are
                  a set of case-sensitive key value pairs. An Elasticsearch
                  domain may have up to 10 tags. See <a
                  href="http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-managedomains.html#es-managedomains-awsresorcetagging"
                  target="_blank"> Tagging Amazon Elasticsearch Service Domains
                  for more information.</a></p>
                tags:
                  - Add
                  - Tags
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
            /2015-01-01/packages/associate/{PackageID}/{DomainName}:
              POST:
                summary: AssociatePackage
                description: <p>Associates a package with an Amazon ES domain.</p>
                tags:
                  - Associate
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
            /2015-01-01/es/domain/{DomainName}/authorizeVpcEndpointAccess:
              POST:
                summary: AuthorizeVpcEndpointAccess
                description: >-
                  <p>Provides access to an Amazon OpenSearch Service domain
                  through the use of an interface VPC endpoint.</p>
                tags:
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
            /2015-01-01/es/domain/{DomainName}/config/cancel:
              POST:
                summary: CancelDomainConfigChange
                description: >-
                  <p>Cancels a pending configuration change on an Amazon
                  OpenSearch Service domain.</p>
                tags:
                  - Cancel
                  - Domains
                  - Configurations
                  - Change
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
            /2015-01-01/es/serviceSoftwareUpdate/cancel:
              POST:
                summary: CancelElasticsearchServiceSoftwareUpdate
                description: >-
                  <p>Cancels a scheduled service software update for an Amazon
                  ES domain. You can only perform this operation before the
                  <code>AutomatedUpdateDate</code> and when the
                  <code>UpdateStatus</code> is in the
                  <code>PENDING_UPDATE</code> state.</p>
                tags:
                  - Cancel
                  - Elasticsearch
                  - Services
                  - Software
                  - Update
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
            /2015-01-01/es/domain:
              POST:
                summary: CreateElasticsearchDomain
                description: >-
                  <p>Creates a new Elasticsearch domain. For more information,
                  see <a
                  href="http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains"
                  target="_blank">Creating Elasticsearch Domains</a> in the
                  <i>Amazon Elasticsearch Service Developer Guide</i>.</p>
                tags:
                  - Create
                  - Elasticsearch
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
            /2015-01-01/es/ccs/outboundConnection:
              POST:
                summary: CreateOutboundCrossClusterSearchConnection
                description: >-
                  <p>Creates a new cross-cluster search connection from a source
                  domain to a destination domain.</p>
                tags:
                  - Create
                  - Outbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
            /2015-01-01/packages:
              POST:
                summary: CreatePackage
                description: <p>Create a package for use with Amazon ES domains.</p>
                tags:
                  - Create
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
            /2015-01-01/es/vpcEndpoints:
              GET:
                summary: ListVpcEndpoints
                description: >-
                  <p>Retrieves all Amazon OpenSearch Service-managed VPC
                  endpoints in the current account and Region.</p>
                tags:
                  - Lists
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
            /2015-01-01/es/domain/{DomainName}:
              GET:
                summary: DescribeElasticsearchDomain
                description: >-
                  <p>Returns domain configuration information about the
                  specified Elasticsearch domain, including the domain ID,
                  domain endpoint, and domain ARN.</p>
                tags:
                  - Describe
                  - Elasticsearch
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
            /2015-01-01/es/role:
              DELETE:
                summary: DeleteElasticsearchServiceRole
                description: >-
                  <p>Deletes the service-linked role that Elasticsearch Service
                  uses to manage and maintain VPC domains. Role deletion will
                  fail if any existing VPC domains use the role. You must delete
                  any such Elasticsearch domains before deleting the role. See
                  <a
                  href="http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-vpc.html#es-enabling-slr"
                  target="_blank">Deleting Elasticsearch Service Role</a> in
                  <i>VPC Endpoints for Amazon Elasticsearch Service
                  Domains</i>.</p>
                tags:
                  - Delete
                  - Elasticsearch
                  - Services
                  - Roles
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
            /2015-01-01/es/ccs/inboundConnection/{ConnectionId}:
              DELETE:
                summary: DeleteInboundCrossClusterSearchConnection
                description: >-
                  <p>Allows the destination domain owner to delete an existing
                  inbound cross-cluster search connection.</p>
                tags:
                  - Delete
                  - Inbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
            /2015-01-01/es/ccs/outboundConnection/{ConnectionId}:
              DELETE:
                summary: DeleteOutboundCrossClusterSearchConnection
                description: >-
                  <p>Allows the source domain owner to delete an existing
                  outbound cross-cluster search connection.</p>
                tags:
                  - Delete
                  - Outbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
            /2015-01-01/packages/{PackageID}:
              DELETE:
                summary: DeletePackage
                description: <p>Delete the package.</p>
                tags:
                  - Delete
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
            /2015-01-01/es/vpcEndpoints/{VpcEndpointId}:
              DELETE:
                summary: DeleteVpcEndpoint
                description: >-
                  <p>Deletes an Amazon OpenSearch Service-managed interface VPC
                  endpoint.</p>
                tags:
                  - Delete
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
            /2015-01-01/es/domain/{DomainName}/autoTunes:
              GET:
                summary: DescribeDomainAutoTunes
                description: >-
                  <p>Provides scheduled Auto-Tune action details for the
                  Elasticsearch domain, such as Auto-Tune action type,
                  description, severity, and scheduled date.</p>
                tags:
                  - Describe
                  - Domains
                  - Auto
                  - Tunes
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
            /2015-01-01/es/domain/{DomainName}/progress:
              GET:
                summary: DescribeDomainChangeProgress
                description: >-
                  <p>Returns information about the current blue/green deployment
                  happening on a domain, including a change ID, status, and
                  progress stages.</p>
                tags:
                  - Describe
                  - Domains
                  - Change
                  - Progress
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
            /2015-01-01/es/domain/{DomainName}/config:
              POST:
                summary: UpdateElasticsearchDomainConfig
                description: >-
                  <p>Modifies the cluster configuration of the specified
                  Elasticsearch domain, setting as setting the instance type and
                  the number of instances. </p>
                tags:
                  - Update
                  - Elasticsearch
                  - Domains
                  - Configurations
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
            /2015-01-01/es/domain-info:
              POST:
                summary: DescribeElasticsearchDomains
                description: >-
                  <p>Returns domain configuration information about the
                  specified Elasticsearch domains, including the domain ID,
                  domain endpoint, and domain ARN.</p>
                tags:
                  - Describe
                  - Elasticsearch
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
            /2015-01-01/es/instanceTypeLimits/{ElasticsearchVersion}/{InstanceType}:
              GET:
                summary: DescribeElasticsearchInstanceTypeLimits
                description: >-
                  <p> Describe Elasticsearch Limits for a given InstanceType and
                  ElasticsearchVersion. When modifying existing Domain, specify
                  the <code> <a>DomainName</a> </code> to know what Limits are
                  supported for modifying. </p>
                tags:
                  - Describe
                  - Elasticsearch
                  - Instances
                  - Types
                  - Limits
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
            /2015-01-01/es/ccs/inboundConnection/search:
              POST:
                summary: DescribeInboundCrossClusterSearchConnections
                description: >-
                  <p>Lists all the inbound cross-cluster search connections for
                  a destination domain.</p>
                tags:
                  - Describe
                  - Inbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
            /2015-01-01/es/ccs/outboundConnection/search:
              POST:
                summary: DescribeOutboundCrossClusterSearchConnections
                description: >-
                  <p>Lists all the outbound cross-cluster search connections for
                  a source domain.</p>
                tags:
                  - Describe
                  - Outbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
            /2015-01-01/packages/describe:
              POST:
                summary: DescribePackages
                description: >-
                  <p>Describes all packages available to Amazon ES. Includes
                  options for filtering, limiting the number of results, and
                  pagination.</p>
                tags:
                  - Describe
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
            /2015-01-01/es/reservedInstanceOfferings:
              GET:
                summary: DescribeReservedElasticsearchInstanceOfferings
                description: >-
                  <p>Lists available reserved Elasticsearch instance
                  offerings.</p>
                tags:
                  - Describe
                  - Reserved
                  - Elasticsearch
                  - Instances
                  - Offerings
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
            /2015-01-01/es/reservedInstances:
              GET:
                summary: DescribeReservedElasticsearchInstances
                description: >-
                  <p>Returns information about reserved Elasticsearch instances
                  for this account.</p>
                tags:
                  - Describe
                  - Reserved
                  - Elasticsearch
                  - Instances
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
            /2015-01-01/es/vpcEndpoints/describe:
              POST:
                summary: DescribeVpcEndpoints
                description: >-
                  <p>Describes one or more Amazon OpenSearch Service-managed VPC
                  endpoints.</p>
                tags:
                  - Describe
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
            /2015-01-01/packages/dissociate/{PackageID}/{DomainName}:
              POST:
                summary: DissociatePackage
                description: <p>Dissociates a package from the Amazon ES domain.</p>
                tags:
                  - Dissociate
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
            /2015-01-01/es/compatibleVersions:
              GET:
                summary: GetCompatibleElasticsearchVersions
                description: >-
                  <p> Returns a list of upgrade compatible Elastisearch
                  versions. You can optionally pass a <code> <a>DomainName</a>
                  </code> to get all upgrade compatible Elasticsearch versions
                  for that specific domain. </p>
                tags:
                  - Get
                  - Compatible
                  - Elasticsearch
                  - Versions
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
            /2015-01-01/packages/{PackageID}/history:
              GET:
                summary: GetPackageVersionHistory
                description: >-
                  <p>Returns a list of versions of the package, along with their
                  creation time and commit message.</p>
                tags:
                  - Get
                  - Packages
                  - Versions
                  - History
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
            /2015-01-01/es/upgradeDomain/{DomainName}/history:
              GET:
                summary: GetUpgradeHistory
                description: >-
                  <p>Retrieves the complete history of the last 10 upgrades that
                  were performed on the domain.</p>
                tags:
                  - Get
                  - Upgrade
                  - History
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
            /2015-01-01/es/upgradeDomain/{DomainName}/status:
              GET:
                summary: GetUpgradeStatus
                description: >-
                  <p>Retrieves the latest status of the last upgrade or upgrade
                  eligibility check that was performed on the domain.</p>
                tags:
                  - Get
                  - Upgrade
                  - Status
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
            /2015-01-01/domain:
              GET:
                summary: ListDomainNames
                description: >-
                  <p>Returns the name of all Elasticsearch domains owned by the
                  current user's account. </p>
                tags:
                  - Lists
                  - Domains
                  - Names
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
            /2015-01-01/packages/{PackageID}/domains:
              GET:
                summary: ListDomainsForPackage
                description: >-
                  <p>Lists all Amazon ES domains associated with the
                  package.</p>
                tags:
                  - Lists
                  - Domains
                  - For
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
            /2015-01-01/es/instanceTypes/{ElasticsearchVersion}:
              GET:
                summary: ListElasticsearchInstanceTypes
                description: >-
                  <p>List all Elasticsearch instance types that are supported
                  for given ElasticsearchVersion</p>
                tags:
                  - Lists
                  - Elasticsearch
                  - Instances
                  - Types
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
            /2015-01-01/es/versions:
              GET:
                summary: ListElasticsearchVersions
                description: <p>List all supported Elasticsearch versions</p>
                tags:
                  - Lists
                  - Elasticsearch
                  - Versions
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
            /2015-01-01/domain/{DomainName}/packages:
              GET:
                summary: ListPackagesForDomain
                description: >-
                  <p>Lists all packages associated with the Amazon ES
                  domain.</p>
                tags:
                  - Lists
                  - Packages
                  - For
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
            /2015-01-01/tags/:
              GET:
                summary: ListTags
                description: <p>Returns all tags for the given Elasticsearch domain.</p>
                tags:
                  - Lists
                  - Tags
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
            /2015-01-01/es/domain/{DomainName}/listVpcEndpointAccess:
              GET:
                summary: ListVpcEndpointAccess
                description: >-
                  <p>Retrieves information about each principal that is allowed
                  to access a given Amazon OpenSearch Service domain through the
                  use of an interface VPC endpoint.</p>
                tags:
                  - Lists
                  - VPC
                  - Endpoints
                  - Access
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
            /2015-01-01/es/domain/{DomainName}/vpcEndpoints:
              GET:
                summary: ListVpcEndpointsForDomain
                description: >-
                  <p>Retrieves all Amazon OpenSearch Service-managed VPC
                  endpoints associated with a particular domain.</p>
                tags:
                  - Lists
                  - VPC
                  - Endpoints
                  - For
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
            /2015-01-01/es/purchaseReservedInstanceOffering:
              POST:
                summary: PurchaseReservedElasticsearchInstanceOffering
                description: >-
                  <p>Allows you to purchase reserved Elasticsearch
                  instances.</p>
                tags:
                  - Purchase
                  - Reserved
                  - Elasticsearch
                  - Instances
                  - Offerings
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
            /2015-01-01/es/ccs/inboundConnection/{ConnectionId}/reject:
              PUT:
                summary: RejectInboundCrossClusterSearchConnection
                description: >-
                  <p>Allows the destination domain owner to reject an inbound
                  cross-cluster search connection request.</p>
                tags:
                  - Reject
                  - Inbound
                  - Cross
                  - Cluster
                  - Search
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
            /2015-01-01/tags-removal:
              POST:
                summary: RemoveTags
                description: >-
                  <p>Removes the specified set of tags from the specified
                  Elasticsearch domain.</p>
                tags:
                  - Removes
                  - Tags
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
            /2015-01-01/es/domain/{DomainName}/revokeVpcEndpointAccess:
              POST:
                summary: RevokeVpcEndpointAccess
                description: >-
                  <p>Revokes access to an Amazon OpenSearch Service domain that
                  was provided through an interface VPC endpoint.</p>
                tags:
                  - Revoke
                  - VPC
                  - Endpoints
                  - Access
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
            /2015-01-01/es/serviceSoftwareUpdate/start:
              POST:
                summary: StartElasticsearchServiceSoftwareUpdate
                description: >-
                  <p>Schedules a service software update for an Amazon ES
                  domain.</p>
                tags:
                  - Start
                  - Elasticsearch
                  - Services
                  - Software
                  - Update
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
            /2015-01-01/packages/update:
              POST:
                summary: UpdatePackage
                description: <p>Updates a package for use with Amazon ES domains.</p>
                tags:
                  - Update
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
            /2015-01-01/es/vpcEndpoints/update:
              POST:
                summary: UpdateVpcEndpoint
                description: >-
                  <p>Modifies an Amazon OpenSearch Service-managed interface VPC
                  endpoint.</p>
                tags:
                  - Update
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
            /2015-01-01/es/upgradeDomain:
              POST:
                summary: UpgradeElasticsearchDomain
                description: >-
                  <p>Allows you to either upgrade your domain or perform an
                  Upgrade eligibility check to a compatible Elasticsearch ve
                tags:
                  - Upgrade
                  - Elasticsearch
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - '2015'
                  - '01'
                  - Tags
                  - Packages
                  - Domains
                  - Names
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Es
                  - Packages
                  - Endpoints
                  - Roles
                  - Auto
                  - Tunes
                  - Progress
                  - Info
                  - Types
                  - Limits
                  - Elasticsearch
                  - Versions
                  - Instances
                  - Search
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - History
                  - Status
                  - Domains
                  - Types
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Sta
    overlays:
      - type: APIs.io Search
        url: overlays/es-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/es-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:es
  - name: kafka
    description: <p>The operations for managing an Amazon MSK cluster.</p>
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
            title: kafka
          paths:
            /v1/clusters/{clusterArn}/scram-secrets:
              GET:
                summary: ListScramSecrets
                description: >-
                  <p>Returns a list of the Scram Secrets associated with an
                  Amazon MSK cluster.</p>
                tags:
                  - Lists
                  - Scram
                  - Secrets
                  - ARN
                  - Scram
                  - Secrets
            /v1/clusters:
              GET:
                summary: ListClusters
                description: >-
                  <p>Returns a list of all the MSK clusters in the current
                  Region.</p>
                tags:
                  - Lists
                  - Clusters
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
            /api/v2/clusters:
              GET:
                summary: ListClustersV2
                description: >-
                  <p>Returns a list of all the MSK clusters in the current
                  Region.</p>
                tags:
                  - Lists
                  - Clusters
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
            /replication/v1/replicators:
              GET:
                summary: ListReplicators
                description: <p>Lists the replicators.</p>
                tags:
                  - Lists
                  - Replicators
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
            /v1/configurations:
              GET:
                summary: ListConfigurations
                description: >-
                  <p>Returns a list of all the MSK configurations in this
                  Region.</p>
                tags:
                  - Lists
                  - Configurations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
            /v1/vpc-connection:
              POST:
                summary: CreateVpcConnection
                description: <p>Creates a new Amazon MSK VPC connection.</p>
                tags:
                  - Create
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
            /v1/clusters/{clusterArn}:
              GET:
                summary: DescribeCluster
                description: >-
                  <p>Returns a description of the MSK cluster whose Amazon
                  Resource Name (ARN) is specified in the request.</p>
                tags:
                  - Describe
                  - Cluster
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
            /v1/clusters/{clusterArn}/policy:
              PUT:
                summary: PutClusterPolicy
                description: >-
                  <p>Creates or updates the specified MSK cluster policy. If
                  updating the policy, the currentVersion field is required in
                  the request payload.</p>
                tags:
                  - Put
                  - Cluster
                  - Policies
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /v1/configurations/{arn}:
              PUT:
                summary: UpdateConfiguration
                description: >-
                  <p>Updates an existing MSK configuration. The configuration
                  must be in the Active state.</p>
                tags:
                  - Update
                  - Configurations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /replication/v1/replicators/{replicatorArn}:
              GET:
                summary: DescribeReplicator
                description: >-
                  <p>Returns a description of the Kafka Replicator whose Amazon
                  Resource Name (ARN) is specified in the request.</p>
                tags:
                  - Describe
                  - Replicators
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /v1/vpc-connection/{arn}:
              GET:
                summary: DescribeVpcConnection
                description: >-
                  <p>Displays information about the specified Amazon MSK VPC
                  connection.</p>
                tags:
                  - Describe
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /api/v2/clusters/{clusterArn}:
              GET:
                summary: DescribeClusterV2
                description: >-
                  <p>Returns a description of the MSK cluster of either the
                  provisioned or the serverless type whose Amazon Resource Name
                  (ARN) is specified in the request.</p>
                tags:
                  - Describe
                  - Cluster
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /v1/operations/{clusterOperationArn}:
              GET:
                summary: DescribeClusterOperation
                description: >-
                  <p>Returns a description of the cluster operation specified by
                  the ARN.</p>
                tags:
                  - Describe
                  - Cluster
                  - Operation
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
            /api/v2/operations/{clusterOperationArn}:
              GET:
                summary: DescribeClusterOperationV2
                description: >-
                  <p>Returns a description of the cluster operation specified by
                  the ARN.</p>
                tags:
                  - Describe
                  - Cluster
                  - Operation
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
            /v1/configurations/{arn}/revisions/{revision}:
              GET:
                summary: DescribeConfigurationRevision
                description: >-
                  <p>Returns a description of this revision of the
                  configuration.</p>
                tags:
                  - Describe
                  - Configurations
                  - Revisions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
            /v1/clusters/{clusterArn}/bootstrap-brokers:
              GET:
                summary: GetBootstrapBrokers
                description: >-
                  <p>A list of brokers that a client application can use to
                  bootstrap.</p>
                tags:
                  - Get
                  - Bootstrap
                  - Brokers
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
            /v1/compatible-kafka-versions:
              GET:
                summary: GetCompatibleKafkaVersions
                description: >-
                  <p>Gets the Apache Kafka versions to which you can update the
                  MSK cluster.</p>
                tags:
                  - Get
                  - Compatible
                  - Kafka
                  - Versions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
            /v1/clusters/{clusterArn}/client-vpc-connections:
              GET:
                summary: ListClientVpcConnections
                description: <p>Displays a list of client VPC connections.</p>
                tags:
                  - Lists
                  - Client
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
            /v1/clusters/{clusterArn}/operations:
              GET:
                summary: ListClusterOperations
                description: >-
                  <p>Returns a list of all the operations that have been
                  performed on the specified MSK cluster.</p>
                tags:
                  - Lists
                  - Cluster
                  - Operations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /api/v2/clusters/{clusterArn}/operations:
              GET:
                summary: ListClusterOperationsV2
                description: >-
                  <p>Returns a list of all the operations that have been
                  performed on the specified MSK cluster.</p>
                tags:
                  - Lists
                  - Cluster
                  - Operations
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /v1/configurations/{arn}/revisions:
              GET:
                summary: ListConfigurationRevisions
                description: >-
                  <p>Returns a list of all the revisions of an MSK
                  configuration.</p>
                tags:
                  - Lists
                  - Configurations
                  - Revisions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /v1/kafka-versions:
              GET:
                summary: ListKafkaVersions
                description: <p>Returns a list of Apache Kafka versions.</p>
                tags:
                  - Lists
                  - Kafka
                  - Versions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /v1/clusters/{clusterArn}/nodes:
              GET:
                summary: ListNodes
                description: <p>Returns a list of the broker nodes in the cluster.</p>
                tags:
                  - Lists
                  - Nodes
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
            /v1/tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes the tags associated with the keys that are provided
                  in the query.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
            /v1/vpc-connections:
              GET:
                summary: ListVpcConnections
                description: <p>Displays a list of Amazon MSK VPC connections.</p>
                tags:
                  - Lists
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
            /v1/clusters/{clusterArn}/reboot-broker:
              PUT:
                summary: RebootBroker
                description: <p>Executes a reboot on a broker.</p>
                tags:
                  - Reboot
                  - Brokers
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
            /v1/clusters/{clusterArn}/nodes/count:
              PUT:
                summary: UpdateBrokerCount
                description: >-
                  <p>Updates the number of broker nodes in the cluster. You can
                  use this operation to increase the number of brokers in an
                  existing cluster. You can't decrease the number of
                  brokers.</p>
                tags:
                  - Update
                  - Brokers
                  - Count
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
            /v1/clusters/{clusterArn}/nodes/type:
              PUT:
                summary: UpdateBrokerType
                description: >-
                  <p>Updates all the brokers in the cluster to the specified
                  type.</p>
                tags:
                  - Update
                  - Brokers
                  - Types
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
            /v1/clusters/{clusterArn}/nodes/storage:
              PUT:
                summary: UpdateBrokerStorage
                description: <p>Updates the EBS storage associated with MSK brokers.</p>
                tags:
                  - Update
                  - Brokers
                  - Storage
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
            /v1/clusters/{clusterArn}/connectivity:
              PUT:
                summary: UpdateConnectivity
                description: >-
                  <p>Updates the connectivity configuration for the MSK
                  cluster.</p>
                tags:
                  - Update
                  - Connectivity
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
            /v1/clusters/{clusterArn}/configuration:
              PUT:
                summary: UpdateClusterConfiguration
                description: >-
                  <p>Updates the cluster with the configuration that is
                  specified in the request body.</p>
                tags:
                  - Update
                  - Cluster
                  - Configurations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
            /v1/clusters/{clusterArn}/version:
              PUT:
                summary: UpdateClusterKafkaVersion
                description: <p>Updates the Apache Kafka version for the cluster.</p>
                tags:
                  - Update
                  - Cluster
                  - Kafka
                  - Versions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
            /v1/clusters/{clusterArn}/monitoring:
              PUT:
                summary: UpdateMonitoring
                description: >-
                  <p>Updates the monitoring settings for the cluster. You can
                  use this operation to specify which Apache Kafka metrics you
                  want Amazon MSK to send to Amazon CloudWatch. You can also
                  specify settings for open monitoring with Prometheus.</p>
                tags:
                  - Update
                  - Monitoring
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
            /replication/v1/replicators/{replicatorArn}/replication-info:
              PUT:
                summary: UpdateReplicationInfo
                description: <p>Updates replication info of a replicator.</p>
                tags:
                  - Update
                  - Replication
                  - Info
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
                  - Info
            /v1/clusters/{clusterArn}/security:
              PATCH:
                summary: UpdateSecurity
                description: >-
                  <p>You can use this operation to update the encrypting and
                  authentication settings for an existing cluster.</p>
                tags:
                  - Update
                  - Security
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
                  - Info
                  - Security
            /v1/clusters/{clusterArn}/storage:
              PUT:
                summary: UpdateStorage
                description: >-
                  <p>Updates cluster broker volume size (or) sets cluster
                  storage mode to T
                tags:
                  - Update
                  - Storage
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
                  - Info
                  - Securi
    overlays:
      - type: APIs.io Search
        url: overlays/kafka-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kafka-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kafka
  - name: opensearch
    description: >-
      <p>Use the Amazon OpenSearch Service configuration API to create,
      configure, and manage OpenSearch Service domains.</p> <p>For sample code
      that uses the configuration API, see the <a
      href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/opensearch-configuration-samples.html">
      <i>Amazon OpenSearch Service Developer Guide</i> </a>. The guide also
      contains <a
      href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/request-signing.html">sample
      code</a> for sending signed HTTP requests to the OpenSearch APIs. The
      endpoint for configuration service requests is Region specific:
      es.<i>region</i>.amazonaws.com. For example, es.us-east-1.amazonaws.com.
      For a current list of supported Regions and endpoints, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/rande.html#service-regions">Amazon
      Web Services service endpoints</a>.</p>
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
            title: opensearch
          paths:
            /2021-01-01/opensearch/cc/inboundConnection/{ConnectionId}/accept:
              PUT:
                summary: AcceptInboundConnection
                description: >-
                  <p>Allows the destination Amazon OpenSearch Service domain
                  owner to accept an inbound cross-cluster search connection
                  request. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html">Cross-cluster
                  search for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Accept
                  - Inbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
            /2021-01-01/opensearch/domain/{DomainName}/dataSource:
              GET:
                summary: ListDataSources
                description: >-
                  <p>Lists direct-query data sources for a specific domain. For
                  more information, see For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/direct-query-s3.html">Working
                  with Amazon OpenSearch Service direct queries with Amazon
                  S3</a>.</p>
                tags:
                  - Lists
                  - Data
                  - Sources
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
            /2021-01-01/tags:
              POST:
                summary: AddTags
                description: >-
                  <p>Attaches tags to an existing Amazon OpenSearch Service
                  domain. Tags are a set of case-sensitive key-value pairs. A
                  domain can have up to 10 tags. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains-awsresourcetagging.html">Tagging
                  Amazon OpenSearch Service domains</a>.</p>
                tags:
                  - Add
                  - Tags
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
            /2021-01-01/packages/associate/{PackageID}/{DomainName}:
              POST:
                summary: AssociatePackage
                description: >-
                  <p>Associates a package with an Amazon OpenSearch Service
                  domain. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Associate
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
            /2021-01-01/opensearch/domain/{DomainName}/authorizeVpcEndpointAccess:
              POST:
                summary: AuthorizeVpcEndpointAccess
                description: >-
                  <p>Provides access to an Amazon OpenSearch Service domain
                  through the use of an interface VPC endpoint.</p>
                tags:
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
            /2021-01-01/opensearch/domain/{DomainName}/config/cancel:
              POST:
                summary: CancelDomainConfigChange
                description: >-
                  <p>Cancels a pending configuration change on an Amazon
                  OpenSearch Service domain.</p>
                tags:
                  - Cancel
                  - Domains
                  - Configurations
                  - Change
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
            /2021-01-01/opensearch/serviceSoftwareUpdate/cancel:
              POST:
                summary: CancelServiceSoftwareUpdate
                description: >-
                  <p>Cancels a scheduled service software update for an Amazon
                  OpenSearch Service domain. You can only perform this operation
                  before the <code>AutomatedUpdateDate</code> and when the
                  domain's <code>UpdateStatus</code> is
                  <code>PENDING_UPDATE</code>. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/service-software.html">Service
                  software updates in Amazon OpenSearch Service</a>.</p>
                tags:
                  - Cancel
                  - Services
                  - Software
                  - Update
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
            /2021-01-01/opensearch/domain:
              POST:
                summary: CreateDomain
                description: >-
                  <p>Creates an Amazon OpenSearch Service domain. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/createupdatedomains.html">Creating
                  and managing Amazon OpenSearch Service domains</a>.</p>
                tags:
                  - Create
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
            /2021-01-01/opensearch/cc/outboundConnection:
              POST:
                summary: CreateOutboundConnection
                description: >-
                  <p>Creates a new cross-cluster search connection from a source
                  Amazon OpenSearch Service domain to a destination domain. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html">Cross-cluster
                  search for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Create
                  - Outbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
            /2021-01-01/packages:
              POST:
                summary: CreatePackage
                description: >-
                  <p>Creates a package for use with Amazon OpenSearch Service
                  domains. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Create
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
            /2021-01-01/opensearch/vpcEndpoints:
              GET:
                summary: ListVpcEndpoints
                description: >-
                  <p>Retrieves all Amazon OpenSearch Service-managed VPC
                  endpoints in the current Amazon Web Services account and
                  Region.</p>
                tags:
                  - Lists
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/opensearch/domain/{DomainName}/dataSource/{DataSourceName}:
              PUT:
                summary: UpdateDataSource
                description: >-
                  <p>Updates a direct-query data source. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/direct-query-s3-creating.html">Working
                  with Amazon OpenSearch Service data source integrations with
                  Amazon S3</a>.</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/opensearch/domain/{DomainName}:
              GET:
                summary: DescribeDomain
                description: >-
                  <p>Describes the domain configuration for the specified Amazon
                  OpenSearch Service domain, including the domain ID, domain
                  service endpoint, and domain ARN.</p>
                tags:
                  - Describe
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/opensearch/cc/inboundConnection/{ConnectionId}:
              DELETE:
                summary: DeleteInboundConnection
                description: >-
                  <p>Allows the destination Amazon OpenSearch Service domain
                  owner to delete an existing inbound cross-cluster search
                  connection. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html">Cross-cluster
                  search for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Delete
                  - Inbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/opensearch/cc/outboundConnection/{ConnectionId}:
              DELETE:
                summary: DeleteOutboundConnection
                description: >-
                  <p>Allows the source Amazon OpenSearch Service domain owner to
                  delete an existing outbound cross-cluster search connection.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html">Cross-cluster
                  search for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Delete
                  - Outbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/packages/{PackageID}:
              DELETE:
                summary: DeletePackage
                description: >-
                  <p>Deletes an Amazon OpenSearch Service package. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Delete
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/opensearch/vpcEndpoints/{VpcEndpointId}:
              DELETE:
                summary: DeleteVpcEndpoint
                description: >-
                  <p>Deletes an Amazon OpenSearch Service-managed interface VPC
                  endpoint.</p>
                tags:
                  - Delete
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
            /2021-01-01/opensearch/domain/{DomainName}/autoTunes:
              GET:
                summary: DescribeDomainAutoTunes
                description: >-
                  <p>Returns the list of optimizations that Auto-Tune has made
                  to an Amazon OpenSearch Service domain. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/auto-tune.html">Auto-Tune
                  for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Domains
                  - Auto
                  - Tunes
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
            /2021-01-01/opensearch/domain/{DomainName}/progress:
              GET:
                summary: DescribeDomainChangeProgress
                description: >-
                  <p>Returns information about the current blue/green deployment
                  happening on an Amazon OpenSearch Service domain. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains-configuration-changes.html">Making
                  configuration changes in Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Domains
                  - Change
                  - Progress
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
            /2021-01-01/opensearch/domain/{DomainName}/config:
              POST:
                summary: UpdateDomainConfig
                description: >-
                  <p>Modifies the cluster configuration of the specified Amazon
                  OpenSearch Service domain.</p>
                tags:
                  - Update
                  - Domains
                  - Configurations
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
            /2021-01-01/opensearch/domain/{DomainName}/health:
              GET:
                summary: DescribeDomainHealth
                description: >-
                  <p>Returns information about domain and node health, the
                  standby Availability Zone, number of nodes per Availability
                  Zone, and shard count per node.</p>
                tags:
                  - Describe
                  - Domains
                  - Health
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
            /2021-01-01/opensearch/domain/{DomainName}/nodes:
              GET:
                summary: DescribeDomainNodes
                description: >-
                  <p>Returns information about domain and nodes, including data
                  nodes, master nodes, ultrawarm nodes, Availability Zone(s),
                  standby nodes, node configurations, and node states.</p>
                tags:
                  - Describe
                  - Domains
                  - Nodes
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
            /2021-01-01/opensearch/domain-info:
              POST:
                summary: DescribeDomains
                description: >-
                  <p>Returns domain configuration information about the
                  specified Amazon OpenSearch Service domains.</p>
                tags:
                  - Describe
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
            /2021-01-01/opensearch/domain/{DomainName}/dryRun:
              GET:
                summary: DescribeDryRunProgress
                description: >-
                  <p>Describes the progress of a pre-update dry run analysis on
                  an Amazon OpenSearch Service domain. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains-configuration-changes#dryrun">Determining
                  whether a change will cause a blue/green deployment</a>.</p>
                tags:
                  - Describe
                  - Dry
                  - Runs
                  - Progress
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
            /2021-01-01/opensearch/cc/inboundConnection/search:
              POST:
                summary: DescribeInboundConnections
                description: >-
                  <p>Lists all the inbound cross-cluster search connections for
                  a destination (remote) Amazon OpenSearch Service domain. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html">Cross-cluster
                  search for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Inbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
            /2021-01-01/opensearch/instanceTypeLimits/{EngineVersion}/{InstanceType}:
              GET:
                summary: DescribeInstanceTypeLimits
                description: >-
                  <p>Describes the instance count, storage, and master node
                  limits for a given OpenSearch or Elasticsearch version and
                  instance type.</p>
                tags:
                  - Describe
                  - Instances
                  - Types
                  - Limits
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
            /2021-01-01/opensearch/cc/outboundConnection/search:
              POST:
                summary: DescribeOutboundConnections
                description: >-
                  <p>Lists all the outbound cross-cluster connections for a
                  local (source) Amazon OpenSearch Service domain. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html">Cross-cluster
                  search for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Outbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
            /2021-01-01/packages/describe:
              POST:
                summary: DescribePackages
                description: >-
                  <p>Describes all packages available to OpenSearch Service. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
            /2021-01-01/opensearch/reservedInstanceOfferings:
              GET:
                summary: DescribeReservedInstanceOfferings
                description: >-
                  <p>Describes the available Amazon OpenSearch Service Reserved
                  Instance offerings for a given Region. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ri.html">Reserved
                  Instances in Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Reserved
                  - Instances
                  - Offerings
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
            /2021-01-01/opensearch/reservedInstances:
              GET:
                summary: DescribeReservedInstances
                description: >-
                  <p>Describes the Amazon OpenSearch Service instances that you
                  have reserved in a given Region. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ri.html">Reserved
                  Instances in Amazon OpenSearch Service</a>.</p>
                tags:
                  - Describe
                  - Reserved
                  - Instances
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
            /2021-01-01/opensearch/vpcEndpoints/describe:
              POST:
                summary: DescribeVpcEndpoints
                description: >-
                  <p>Describes one or more Amazon OpenSearch Service-managed VPC
                  endpoints.</p>
                tags:
                  - Describe
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
            /2021-01-01/packages/dissociate/{PackageID}/{DomainName}:
              POST:
                summary: DissociatePackage
                description: >-
                  <p>Removes a package from the specified Amazon OpenSearch
                  Service domain. The package can't be in use with any
                  OpenSearch index for the dissociation to succeed. The package
                  is still available in OpenSearch Service for association
                  later. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Dissociate
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
            /2021-01-01/opensearch/compatibleVersions:
              GET:
                summary: GetCompatibleVersions
                description: >-
                  <p>Returns a map of OpenSearch or Elasticsearch versions and
                  the versions you can upgrade them to.</p>
                tags:
                  - Get
                  - Compatible
                  - Versions
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
            /2021-01-01/opensearch/domain/{DomainName}/domainMaintenance:
              POST:
                summary: StartDomainMaintenance
                description: >-
                  <p>Starts the node maintenance process on the data node. These
                  processes can include a node reboot, an Opensearch or
                  Elasticsearch process restart, or a Dashboard or Kibana
                  restart.</p>
                tags:
                  - Start
                  - Domains
                  - Maintenance
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
            /2021-01-01/packages/{PackageID}/history:
              GET:
                summary: GetPackageVersionHistory
                description: >-
                  <p>Returns a list of Amazon OpenSearch Service package
                  versions, along with their creation time, commit message, and
                  plugin properties (if the package is a zip plugin package).
                  For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Get
                  - Packages
                  - Versions
                  - History
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
            /2021-01-01/opensearch/upgradeDomain/{DomainName}/history:
              GET:
                summary: GetUpgradeHistory
                description: >-
                  <p>Retrieves the complete history of the last 10 upgrades
                  performed on an Amazon OpenSearch Service domain.</p>
                tags:
                  - Get
                  - Upgrade
                  - History
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
            /2021-01-01/opensearch/upgradeDomain/{DomainName}/status:
              GET:
                summary: GetUpgradeStatus
                description: >-
                  <p>Returns the most recent status of the last upgrade or
                  upgrade eligibility check performed on an Amazon OpenSearch
                  Service domain.</p>
                tags:
                  - Get
                  - Upgrade
                  - Status
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
            /2021-01-01/opensearch/domain/{DomainName}/domainMaintenances:
              GET:
                summary: ListDomainMaintenances
                description: <p>A list of maintenance actions for the domain.</p>
                tags:
                  - Lists
                  - Domains
                  - Maintenances
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
            /2021-01-01/domain:
              GET:
                summary: ListDomainNames
                description: >-
                  <p>Returns the names of all Amazon OpenSearch Service domains
                  owned by the current user in the active Region.</p>
                tags:
                  - Lists
                  - Domains
                  - Names
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
            /2021-01-01/packages/{PackageID}/domains:
              GET:
                summary: ListDomainsForPackage
                description: >-
                  <p>Lists all Amazon OpenSearch Service domains associated with
                  a given package. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Lists
                  - Domains
                  - For
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
            /2021-01-01/opensearch/instanceTypeDetails/{EngineVersion}:
              GET:
                summary: ListInstanceTypeDetails
                description: >-
                  <p>Lists all instance types and available features for a given
                  OpenSearch or Elasticsearch version.</p>
                tags:
                  - Lists
                  - Instances
                  - Types
                  - Details
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
            /2021-01-01/domain/{DomainName}/packages:
              GET:
                summary: ListPackagesForDomain
                description: >-
                  <p>Lists all packages associated with an Amazon OpenSearch
                  Service domain. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Lists
                  - Packages
                  - For
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
            /2021-01-01/opensearch/domain/{DomainName}/scheduledActions:
              GET:
                summary: ListScheduledActions
                description: >-
                  <p>Retrieves a list of configuration changes that are
                  scheduled for a domain. These changes can be <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/service-software.html">service
                  software updates</a> or <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/auto-tune.html#auto-tune-types">blue/green
                  Auto-Tune enhancements</a>.</p>
                tags:
                  - Lists
                  - Scheduled
                  - Actions
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
            /2021-01-01/tags/:
              GET:
                summary: ListTags
                description: >-
                  <p>Returns all resource tags for an Amazon OpenSearch Service
                  domain. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains-awsresourcetagging.html">Tagging
                  Amazon OpenSearch Service domains</a>.</p>
                tags:
                  - Lists
                  - Tags
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
            /2021-01-01/opensearch/versions:
              GET:
                summary: ListVersions
                description: >-
                  <p>Lists all versions of OpenSearch and Elasticsearch that
                  Amazon OpenSearch Service supports.</p>
                tags:
                  - Lists
                  - Versions
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
            /2021-01-01/opensearch/domain/{DomainName}/listVpcEndpointAccess:
              GET:
                summary: ListVpcEndpointAccess
                description: >-
                  <p>Retrieves information about each Amazon Web Services
                  principal that is allowed to access a given Amazon OpenSearch
                  Service domain through the use of an interface VPC
                  endpoint.</p>
                tags:
                  - Lists
                  - VPC
                  - Endpoints
                  - Access
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
            /2021-01-01/opensearch/domain/{DomainName}/vpcEndpoints:
              GET:
                summary: ListVpcEndpointsForDomain
                description: >-
                  <p>Retrieves all Amazon OpenSearch Service-managed VPC
                  endpoints associated with a particular domain.</p>
                tags:
                  - Lists
                  - VPC
                  - Endpoints
                  - For
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
            /2021-01-01/opensearch/purchaseReservedInstanceOffering:
              POST:
                summary: PurchaseReservedInstanceOffering
                description: >-
                  <p>Allows you to purchase Amazon OpenSearch Service Reserved
                  Instances.</p>
                tags:
                  - Purchase
                  - Reserved
                  - Instances
                  - Offerings
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
            /2021-01-01/opensearch/cc/inboundConnection/{ConnectionId}/reject:
              PUT:
                summary: RejectInboundConnection
                description: >-
                  <p>Allows the remote Amazon OpenSearch Service domain owner to
                  reject an inbound cross-cluster connection request.</p>
                tags:
                  - Reject
                  - Inbound
                  - Connections
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
            /2021-01-01/tags-removal:
              POST:
                summary: RemoveTags
                description: >-
                  <p>Removes the specified set of tags from an Amazon OpenSearch
                  Service domain. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains.html#managedomains-awsresorcetagging">
                  Tagging Amazon OpenSearch Service domains</a>.</p>
                tags:
                  - Removes
                  - Tags
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
            /2021-01-01/opensearch/domain/{DomainName}/revokeVpcEndpointAccess:
              POST:
                summary: RevokeVpcEndpointAccess
                description: >-
                  <p>Revokes access to an Amazon OpenSearch Service domain that
                  was provided through an interface VPC endpoint.</p>
                tags:
                  - Revoke
                  - VPC
                  - Endpoints
                  - Access
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
            /2021-01-01/opensearch/serviceSoftwareUpdate/start:
              POST:
                summary: StartServiceSoftwareUpdate
                description: >-
                  <p>Schedules a service software update for an Amazon
                  OpenSearch Service domain. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/service-software.html">Service
                  software updates in Amazon OpenSearch Service</a>.</p>
                tags:
                  - Start
                  - Services
                  - Software
                  - Update
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
            /2021-01-01/packages/update:
              POST:
                summary: UpdatePackage
                description: >-
                  <p>Updates a package for use with Amazon OpenSearch Service
                  domains. For more information, see <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html">Custom
                  packages for Amazon OpenSearch Service</a>.</p>
                tags:
                  - Update
                  - Packages
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
            /2021-01-01/opensearch/domain/{DomainName}/scheduledAction/update:
              PUT:
                summary: UpdateScheduledAction
                description: >-
                  <p>Reschedules a planned domain configuration change for a
                  later time. This change can be a scheduled <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/service-software.html">service
                  software update</a> or a <a
                  href="https://docs.aws.amazon.com/opensearch-service/latest/developerguide/auto-tune.html#auto-tune-types">blue/green
                  Auto-Tune enhancement</a>.</p>
                tags:
                  - Update
                  - Scheduled
                  - Actions
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
                  - Actions
            /2021-01-01/opensearch/vpcEndpoints/update:
              POST:
                summary: UpdateVpcEndpoint
                description: >-
                  <p>Modifies an Amazon OpenSearch Service-managed interface VPC
                  endpoint.</p>
                tags:
                  - Update
                  - VPC
                  - Endpoints
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
                  - Actions
            /2021-01-01/opensearch/upgradeDomain:
              POST:
                summary: UpgradeDomain
                description: >-
                  <p>Allows you to either upgrade your Amazon OpenSearch Service
                  domain or perform an upgrade eligibility check to a compatible
                  version of OpenSearch or Elastics
                tags:
                  - Upgrade
                  - Domains
                  - Connections
                  - Identifiers
                  - Accept
                  - Domains
                  - Names
                  - Data
                  - Source
                  - '2021'
                  - '01'
                  - Tags
                  - Packages
                  - Authorize
                  - VPC
                  - Endpoints
                  - Access
                  - Configurations
                  - Cancel
                  - Software
                  - Update
                  - Open Search
                  - Packages
                  - Endpoints
                  - Auto
                  - Tunes
                  - Progress
                  - Health
                  - Nodes
                  - Info
                  - Dry
                  - Runs
                  - Search
                  - Types
                  - Limits
                  - Engines
                  - Versions
                  - Instances
                  - Describe
                  - Offerings
                  - Instances
                  - Versions
                  - Maintenance
                  - History
                  - Status
                  - Maintenances
                  - Domains
                  - Details
                  - Scheduled
                  - Actions
                  - Lists
                  - Reserved
                  - Offerings
                  - Reject
                  - Removal
                  - Revoke
                  - Start
                  - Acti
    overlays:
      - type: APIs.io Search
        url: overlays/opensearch-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/opensearch-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:opensearch
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---