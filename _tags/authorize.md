---
name: Authorize
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/authorize.png
url: https://example.com/apis/authorize.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Authorize
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
  - aid: box:box-authorize-api
    name: Box Authorize API
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.box.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.box.com/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Box Authorize API
          paths:
            /authorize:
              get:
                summary: Authorize user
                description: >-
                  Authorize a user by sending them through the
                  [Box](https://box.com)

                  website and request their permission to act on their behalf.


                  This is the first step when authenticating a user using

                  OAuth 2.0. To request a user's authorization to use the Box
                  APIs

                  on their behalf you will need to send a user to the URL with
                  this

                  format.
                tags:
                  - Authorize
                  - User
                  - Authori
    overlays:
      - type: APIs.io Search
        url: overlays/authorize-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/authorize-openapi-api-evangelist-ratings.yml
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