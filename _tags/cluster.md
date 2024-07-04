---
name: Cluster
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cluster.png
url: https://example.com/apis/cluster.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cluster
apis:
  - name: docdb-elastic
    description: <p>The new Amazon Elastic DocumentDB service endpoint.</p>
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
            title: docdb-elastic
          paths:
            /cluster:
              POST:
                summary: CreateCluster
                description: >-
                  <p>Creates a new Elastic DocumentDB cluster and returns its
                  Cluster structure.</p>
                tags:
                  - Create
                  - Cluster
                  - Cluster
            /cluster-snapshot:
              POST:
                summary: CreateClusterSnapshot
                description: <p>Creates a snapshot of a cluster.</p>
                tags:
                  - Create
                  - Cluster
                  - Snapshots
                  - Cluster
                  - Snapshots
            /cluster/{clusterArn}:
              PUT:
                summary: UpdateCluster
                description: >-
                  <p>Modifies a Elastic DocumentDB cluster. This includes
                  updating admin-username/password, upgrading API version
                  setting up a backup window and maintenance window</p>
                tags:
                  - Update
                  - Cluster
                  - Cluster
                  - Snapshots
                  - ARN
            /cluster-snapshot/{snapshotArn}:
              GET:
                summary: GetClusterSnapshot
                description: >-
                  <p>Returns information about a specific Elastic DocumentDB
                  snapshot</p>
                tags:
                  - Get
                  - Cluster
                  - Snapshots
                  - Cluster
                  - Snapshots
                  - ARN
            /cluster-snapshots:
              GET:
                summary: ListClusterSnapshots
                description: >-
                  <p>Returns information about Elastic DocumentDB snapshots for
                  a specified cluster.</p>
                tags:
                  - Lists
                  - Cluster
                  - Snapshots
                  - Cluster
                  - Snapshots
                  - ARN
                  - Snapshots
            /clusters:
              GET:
                summary: ListClusters
                description: >-
                  <p>Returns information about provisioned Elastic DocumentDB
                  clusters.</p>
                tags:
                  - Lists
                  - Clusters
                  - Cluster
                  - Snapshots
                  - ARN
                  - Snapshots
                  - Clusters
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes metadata tags to a Elastic DocumentDB resource</p>
                tags:
                  - Untag
                  - Resources
                  - Cluster
                  - Snapshots
                  - ARN
                  - Snapshots
                  - Clusters
            /cluster-snapshot/{snapshotArn}/restore:
              POST:
                summary: RestoreClusterFromSnapshot
                description: <p>Restores a Elastic DocumentDB cluster from a sna
                tags:
                  - Restore
                  - Cluster
                  - From
                  - Snapshots
                  - Cluster
                  - Snapshots
                  - ARN
                  - Snapshots
                  - Clusters
                  - Resto
    overlays:
      - type: APIs.io Search
        url: overlays/docdb-elastic-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/docdb-elastic-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:docdb-elastic
  - name: eks
    description: >-
      <p>Amazon Elastic Kubernetes Service (Amazon EKS) is a managed service
      that makes it easy for you to run Kubernetes on Amazon Web Services
      without needing to setup or maintain your own Kubernetes control plane.
      Kubernetes is an open-source system for automating the deployment,
      scaling, and management of containerized applications.</p> <p>Amazon EKS
      runs up-to-date versions of the open-source Kubernetes software, so you
      can use all the existing plugins and tooling from the Kubernetes
      community. Applications running on Amazon EKS are fully compatible with
      applications running on any standard Kubernetes environment, whether
      running in on-premises data centers or public clouds. This means that you
      can easily migrate any standard Kubernetes application to Amazon EKS
      without any code modification required.</p>
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
            title: eks
          paths:
            /clusters/{name}/access-entries/{principalArn}/access-policies:
              GET:
                summary: ListAssociatedAccessPolicies
                description: >-
                  <p>Lists the access policies associated with an access
                  entry.</p>
                tags:
                  - Lists
                  - Associated
                  - Access
                  - Policies
                  - ARN
                  - Access
                  - Policies
            /clusters/{name}/encryption-config/associate:
              POST:
                summary: AssociateEncryptionConfig
                description: >-
                  <p>Associates an encryption configuration to an existing
                  cluster.</p> <p>Use this API to enable encryption on existing
                  clusters that don't already have encryption enabled. This
                  allows you to implement a defense-in-depth security strategy
                  without migrating applications to new Amazon EKS clusters.</p>
                tags:
                  - Associate
                  - Encryption
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
            /clusters/{name}/identity-provider-configs/associate:
              POST:
                summary: AssociateIdentityProviderConfig
                description: >-
                  <p>Associates an identity provider configuration to a
                  cluster.</p> <p>If you want to authenticate identities using
                  an identity provider, you can create an identity provider
                  configuration and associate it to your cluster. After
                  configuring authentication to your cluster you can create
                  Kubernetes <code>Role</code> and <code>ClusterRole</code>
                  objects, assign permissions to them, and then bind them to the
                  identities using Kubernetes <code>RoleBinding</code> and
                  <code>ClusterRoleBinding</code> objects. For more information
                  see <a
                  href="https://kubernetes.io/docs/reference/access-authn-authz/rbac/">Using
                  RBAC Authorization</a> in the Kubernetes documentation.</p>
                tags:
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
            /clusters/{name}/access-entries:
              GET:
                summary: ListAccessEntries
                description: <p>Lists the access entries for your cluster.</p>
                tags:
                  - Lists
                  - Access
                  - Entries
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
            /clusters/{name}/addons:
              GET:
                summary: ListAddons
                description: <p>Lists the installed add-ons.</p>
                tags:
                  - Lists
                  - Addons
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
            /clusters:
              GET:
                summary: ListClusters
                description: >-
                  <p>Lists the Amazon EKS clusters in your Amazon Web Services
                  account in the specified Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Clusters
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
            /eks-anywhere-subscriptions:
              GET:
                summary: ListEksAnywhereSubscriptions
                description: <p>Displays the full description of the subscription.</p>
                tags:
                  - Lists
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
            /clusters/{name}/fargate-profiles:
              GET:
                summary: ListFargateProfiles
                description: >-
                  <p>Lists the Fargate profiles associated with the specified
                  cluster in your Amazon Web Services account in the specified
                  Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Fargate
                  - Profiles
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
            /clusters/{name}/node-groups:
              GET:
                summary: ListNodegroups
                description: >-
                  <p>Lists the managed node groups associated with the specified
                  cluster in your Amazon Web Services account in the specified
                  Amazon Web Services Region. Self-managed node groups aren't
                  listed.</p>
                tags:
                  - Lists
                  - Node Groups
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
            /clusters/{name}/pod-identity-associations:
              GET:
                summary: ListPodIdentityAssociations
                description: >-
                  <p>List the EKS Pod Identity associations in a cluster. You
                  can filter the list by the namespace that the association is
                  in or the service account that the association uses.</p>
                tags:
                  - Lists
                  - Pods
                  - Identity
                  - Associations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /clusters/{name}/access-entries/{principalArn}:
              POST:
                summary: UpdateAccessEntry
                description: <p>Updates an access entry.</p>
                tags:
                  - Update
                  - Access
                  - Entry
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /clusters/{name}/addons/{addonName}:
              GET:
                summary: DescribeAddon
                description: <p>Describes an Amazon EKS add-on.</p>
                tags:
                  - Describe
                  - Addon
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /clusters/{name}:
              GET:
                summary: DescribeCluster
                description: >-
                  <p>Describes an Amazon EKS cluster.</p> <p>The API server
                  endpoint and certificate authority data returned by this
                  operation are required for <code>kubelet</code> and
                  <code>kubectl</code> to communicate with your Kubernetes API
                  server. For more information, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/create-kubeconfig.html">Creating
                  or updating a <code>kubeconfig</code> file for an Amazon EKS
                  cluster</a>.</p> <note> <p>The API server endpoint and
                  certificate authority data aren't available until the cluster
                  reaches the <code>ACTIVE</code> state.</p> </note>
                tags:
                  - Describe
                  - Cluster
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /eks-anywhere-subscriptions/{id}:
              POST:
                summary: UpdateEksAnywhereSubscription
                description: >-
                  <p>Update an EKS Anywhere Subscription. Only auto renewal and
                  tags can be updated after subscription creation.</p>
                tags:
                  - Update
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
            /clusters/{name}/fargate-profiles/{fargateProfileName}:
              GET:
                summary: DescribeFargateProfile
                description: <p>Describes an Fargate profile.</p>
                tags:
                  - Describe
                  - Fargate
                  - Profiles
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
            /clusters/{name}/node-groups/{nodegroupName}:
              GET:
                summary: DescribeNodegroup
                description: <p>Describes a managed node group.</p>
                tags:
                  - Describe
                  - Node Groups
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
            /clusters/{name}/pod-identity-associations/{associationId}:
              POST:
                summary: UpdatePodIdentityAssociation
                description: >-
                  <p>Updates a EKS Pod Identity association. Only the IAM role
                  can be changed; an association can't be moved between
                  clusters, namespaces, or service accounts. If you need to edit
                  the namespace or service account, you need to delete the
                  association and then create a new association with your
                  desired settings.</p>
                tags:
                  - Update
                  - Pods
                  - Identity
                  - Association
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
            /cluster-registrations/{name}:
              DELETE:
                summary: DeregisterCluster
                description: >-
                  <p>Deregisters a connected cluster to remove it from the
                  Amazon EKS control plane.</p> <p>A connected cluster is a
                  Kubernetes cluster that you've connected to your control plane
                  using the <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/eks-connector.html">Amazon
                  EKS Connector</a>.</p>
                tags:
                  - Deregister
                  - Cluster
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
            /addons/configuration-schemas:
              GET:
                summary: DescribeAddonConfiguration
                description: <p>Returns configuration options.</p>
                tags:
                  - Describe
                  - Addon
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
            /addons/supported-versions:
              GET:
                summary: DescribeAddonVersions
                description: >-
                  <p>Describes the versions for an add-on.</p> <p>Information
                  such as the Kubernetes versions that you can use the add-on
                  with, the <code>owner</code>, <code>publisher</code>, and the
                  <code>type</code> of the add-on are returned.</p>
                tags:
                  - Describe
                  - Addon
                  - Versions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
            /clusters/{name}/identity-provider-configs/describe:
              POST:
                summary: DescribeIdentityProviderConfig
                description: <p>Describes an identity provider configuration.</p>
                tags:
                  - Describe
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
            /clusters/{name}/insights/{id}:
              GET:
                summary: DescribeInsight
                description: >-
                  <p>Returns details about an insight that you specify using its
                  ID.</p>
                tags:
                  - Describe
                  - Insight
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
            /clusters/{name}/updates/{updateId}:
              GET:
                summary: DescribeUpdate
                description: >-
                  <p>Describes an update to an Amazon EKS resource.</p> <p>When
                  the status of the update is <code>Succeeded</code>, the update
                  is complete. If an update fails, the status is
                  <code>Failed</code>, and an error detail explains the reason
                  for the failure.</p>
                tags:
                  - Describe
                  - Update
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
            /clusters/{name}/access-entries/{principalArn}/access-policies/{policyArn}:
              DELETE:
                summary: DisassociateAccessPolicy
                description: <p>Disassociates an access policy from an access entry.</p>
                tags:
                  - Disassociate
                  - Access
                  - Policies
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
            /clusters/{name}/identity-provider-configs/disassociate:
              POST:
                summary: DisassociateIdentityProviderConfig
                description: >-
                  <p>Disassociates an identity provider configuration from a
                  cluster.</p> <p>If you disassociate an identity provider from
                  your cluster, users included in the provider can no longer
                  access the cluster. However, you can still access the cluster
                  with IAM principals.</p>
                tags:
                  - Disassociate
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /access-policies:
              GET:
                summary: ListAccessPolicies
                description: <p>Lists the available access policies. </p>
                tags:
                  - Lists
                  - Access
                  - Policies
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /clusters/{name}/identity-provider-configs:
              GET:
                summary: ListIdentityProviderConfigs
                description: >-
                  <p>Lists the identity provider configurations for your
                  cluster.</p>
                tags:
                  - Lists
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /clusters/{name}/insights:
              POST:
                summary: ListInsights
                description: >-
                  <p>Returns a list of all insights checked for against the
                  specified cluster. You can filter which insights are returned
                  by category, associated Kubernetes version, and status.</p>
                tags:
                  - Lists
                  - Insights
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deletes specified tags from an Amazon EKS resource.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /clusters/{name}/updates:
              POST:
                summary: UpdateClusterVersion
                description: >-
                  <p>Updates an Amazon EKS cluster to the specified Kubernetes
                  version. Your cluster continues to function during the update.
                  The response output includes an update ID that you can use to
                  track the status of your cluster update with the
                  <a>DescribeUpdate</a> API operation.</p> <p>Cluster updates
                  are asynchronous, and they should finish within a few minutes.
                  During an update, the cluster status moves to
                  <code>UPDATING</code> (this status transition is eventually
                  consistent). When the update is complete (either
                  <code>Failed</code> or <code>Successful</code>), the cluster
                  status moves to <code>Active</code>.</p> <p>If your cluster
                  has managed node groups attached to it, all of your node
                  groups’ Kubernetes versions must match the cluster’s
                  Kubernetes version in order to update the cluster to a new
                  Kubernetes version.</p>
                tags:
                  - Update
                  - Cluster
                  - Versions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
            /cluster-registrations:
              POST:
                summary: RegisterCluster
                description: >-
                  <p>Connects a Kubernetes cluster to the Amazon EKS control
                  plane. </p> <p>Any Kubernetes cluster can be connected to the
                  Amazon EKS control plane to view current information about the
                  cluster and its nodes. </p> <p>Cluster connection requires two
                  steps. First, send a <code> <a>RegisterClusterRequest</a>
                  </code> to add it to the Amazon EKS control plane.</p>
                  <p>Second, a <a
                  href="https://amazon-eks.s3.us-west-2.amazonaws.com/eks-connector/manifests/eks-connector/latest/eks-connector.yaml">Manifest</a>
                  containing the <code>activationID</code> and
                  <code>activationCode</code> must be applied to the Kubernetes
                  cluster through it's native provider to provide
                  visibility.</p> <p>After the manifest is updated and applied,
                  the connected cluster is visible to the Amazon EKS control
                  plane. If the manifest isn't applied within three days, the
                  connected cluster will no longer be visible and must be
                  deregistered using <code>DeregisterCluster</code>.</p>
                tags:
                  - Register
                  - Cluster
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
            /clusters/{name}/addons/{addonName}/update:
              POST:
                summary: UpdateAddon
                description: <p>Updates an Amazon EKS add-on.</p>
                tags:
                  - Update
                  - Addon
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
            /clusters/{name}/update-config:
              POST:
                summary: UpdateClusterConfig
                description: >-
                  <p>Updates an Amazon EKS cluster configuration. Your cluster
                  continues to function during the update. The response output
                  includes an update ID that you can use to track the status of
                  your cluster update with
                  <code>DescribeUpdate</code>"/&gt;.</p> <p>You can use this API
                  operation to enable or disable exporting the Kubernetes
                  control plane logs for your cluster to CloudWatch Logs. By
                  default, cluster control plane logs aren't exported to
                  CloudWatch Logs. For more information, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/control-plane-logs.html">Amazon
                  EKS Cluster control plane logs</a> in the <i> <i>Amazon EKS
                  User Guide</i> </i>.</p> <note> <p>CloudWatch Logs ingestion,
                  archive storage, and data scanning rates apply to exported
                  control plane logs. For more information, see <a
                  href="http://aws.amazon.com/cloudwatch/pricing/">CloudWatch
                  Pricing</a>.</p> </note> <p>You can also use this API
                  operation to enable or disable public and private access to
                  your cluster's Kubernetes API server endpoint. By default,
                  public access is enabled, and private access is disabled. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/cluster-endpoint.html">Amazon
                  EKS cluster endpoint access control</a> in the <i> <i>Amazon
                  EKS User Guide</i> </i>.</p> <p>You can also use this API
                  operation to choose different subnets and security groups for
                  the cluster. You must specify at least two subnets that are in
                  different Availability Zones. You can't change which VPC the
                  subnets are from, the subnets must be in the same VPC as the
                  subnets that the cluster was created with. For more
                  information about the VPC requirements, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html">https://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html</a>
                  in the <i> <i>Amazon EKS User Guide</i> </i>.</p> <p>Cluster
                  updates are asynchronous, and they should finish within a few
                  minutes. During an update, the cluster status moves to
                  <code>UPDATING</code> (this status transition is eventually
                  consistent). When the update is complete (either
                  <code>Failed</code> or <code>Successful</code>), the cluster
                  status moves to <code>Active</code>.</p>
                tags:
                  - Update
                  - Cluster
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
            /clusters/{name}/node-groups/{nodegroupName}/update-config:
              POST:
                summary: UpdateNodegroupConfig
                description: >-
                  <p>Updates an Amazon EKS managed node group configuration.
                  Your node group continues to function during the update. The
                  response output includes an update ID that you can use to
                  track the status of your node group update with the
                  <a>DescribeUpdate</a> API operation. Currently you can update
                  the Kubernetes labels for a node group or the scaling
                  configuration.</p>
                tags:
                  - Update
                  - Node Groups
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
            /clusters/{name}/node-groups/{nodegroupName}/update-version:
              POST:
                summary: UpdateNodegroupVersion
                description: >-
                  <p>Updates the Kubernetes version or AMI version of an Amazon
                  EKS managed node group.</p> <p>You can update a node group
                  using a launch template only if the node group was originally
                  deployed with a launch template. If you need to update a
                  custom AMI in a node group that was deployed with a launch
                  template, then update your custom AMI, specify the new ID in a
                  new version of the launch template, and then update the node
                  group to the new version of the launch template.</p> <p>If you
                  update without a launch template, then you can update to the
                  latest available AMI version of a node group's current
                  Kubernetes version by not specifying a Kubernetes version in
                  the request. You can update to the latest AMI version of your
                  cluster's current Kubernetes version by specifying your
                  cluster's Kubernetes version in the request. For information
                  about Linux versions, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/eks-linux-ami-versions.html">Amazon
                  EKS optimized Amazon Linux AMI versions</a> in the <i>Amazon
                  EKS User Guide</i>. For information about Windows versions,
                  see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/eks-ami-versions-windows.html">Amazon
                  EKS optimized Windows AMI versions</a> in the <i>Amazon EKS
                  User Guide</i>. </p> <p>You cannot roll back a node group to
                  an earlier Kubernetes version or AMI version.</p> <p>When a
                  node in a managed node group is terminated due to a scaling
                  action or update, every <code>Pod</code> on that node is
                  drained first. Amazon EKS attempts to drain the nodes
                  gracefully and will fail if it is unable to do so. You can
                  <code>force</code> the update if Amazon EKS is unable to drain
                  the nodes as a result of a <code>Pod</code> disruption budget 
                tags:
                  - Update
                  - Node Groups
                  - Versions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
                  - Versions
    overlays:
      - type: APIs.io Search
        url: overlays/eks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/eks-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:eks
  - name: emr-containers
    description: >-
      <p>Amazon EMR on EKS provides a deployment option for Amazon EMR that
      allows you to run open-source big data frameworks on Amazon Elastic
      Kubernetes Service (Amazon EKS). With this deployment option, you can
      focus on running analytics workloads while Amazon EMR on EKS builds,
      configures, and manages containers for open-source applications. For more
      information about Amazon EMR on EKS concepts and tasks, see <a
      href="https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/emr-eks.html">What
      is shared id="EMR-EKS"/&gt;</a>.</p> <p> <i>Amazon EMR containers</i> is
      the API name for Amazon EMR on EKS. The <code>emr-containers</code> prefix
      is used in the following scenarios: </p> <ul> <li> <p>It is the prefix in
      the CLI commands for Amazon EMR on EKS. For example, <code>aws
      emr-containers start-job-run</code>.</p> </li> <li> <p>It is the prefix
      before IAM policy actions for Amazon EMR on EKS. For example,
      <code>"Action": [ "emr-containers:StartJobRun"]</code>. For more
      information, see <a
      href="https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/security_iam_service-with-iam.html#security_iam_service-with-iam-id-based-policies-actions">Policy
      actions for Amazon EMR on EKS</a>.</p> </li> <li> <p>It is the prefix used
      in Amazon EMR on EKS service endpoints. For example,
      <code>emr-containers.us-east-2.amazonaws.com</code>. For more information,
      see <a
      href="https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/service-quotas.html#service-endpoints">Amazon
      EMR on EKSService Endpoints</a>.</p> </li> </ul>
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
            title: emr-containers
          paths:
            /virtualclusters/{virtualClusterId}/jobruns/{jobRunId}:
              GET:
                summary: DescribeJobRun
                description: >-
                  <p>Displays detailed information about a job run. A job run is
                  a unit of work, such as a Spark jar, PySpark script, or
                  SparkSQL query, that you submit to Amazon EMR on EKS.</p>
                tags:
                  - Describe
                  - Jobs
                  - Runs
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
            /jobtemplates:
              GET:
                summary: ListJobTemplates
                description: >-
                  <p>Lists job templates based on a set of parameters. Job
                  template stores values of StartJobRun API request in a
                  template and can be used to start a job run. Job template
                  allows two use cases: avoid repeating recurring StartJobRun
                  API request values, enforcing certain values in StartJobRun
                  API request.</p>
                tags:
                  - Lists
                  - Jobs
                  - Templates
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
            /virtualclusters/{virtualClusterId}/endpoints:
              GET:
                summary: ListManagedEndpoints
                description: >-
                  <p>Lists managed endpoints based on a set of parameters. A
                  managed endpoint is a gateway that connects Amazon EMR Studio
                  to Amazon EMR on EKS so that Amazon EMR Studio can communicate
                  with your virtual cluster.</p>
                tags:
                  - Lists
                  - Managed
                  - Endpoints
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
            /virtualclusters:
              GET:
                summary: ListVirtualClusters
                description: >-
                  <p>Lists information about the specified virtual cluster.
                  Virtual cluster is a managed entity on Amazon EMR on EKS. You
                  can create, describe, list and delete virtual clusters. They
                  do not consume any additional resource in your system. A
                  single virtual cluster maps to a single Kubernetes namespace.
                  Given this relationship, you can model virtual clusters the
                  same way you model Kubernetes namespaces to meet your
                  requirements.</p>
                tags:
                  - Lists
                  - Virtual
                  - Clusters
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
            /jobtemplates/{templateId}:
              GET:
                summary: DescribeJobTemplate
                description: >-
                  <p>Displays detailed information about a specified job
                  template. Job template stores values of StartJobRun API
                  request in a template and can be used to start a job run. Job
                  template allows two use cases: avoid repeating recurring
                  StartJobRun API request values, enforcing certain values in
                  StartJobRun API request.</p>
                tags:
                  - Describe
                  - Jobs
                  - Templates
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
            /virtualclusters/{virtualClusterId}/endpoints/{endpointId}:
              GET:
                summary: DescribeManagedEndpoint
                description: >-
                  <p>Displays detailed information about a managed endpoint. A
                  managed endpoint is a gateway that connects Amazon EMR Studio
                  to Amazon EMR on EKS so that Amazon EMR Studio can communicate
                  with your virtual cluster.</p>
                tags:
                  - Describe
                  - Managed
                  - Endpoints
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
                  - Endpoints
            /virtualclusters/{virtualClusterId}:
              GET:
                summary: DescribeVirtualCluster
                description: >-
                  <p>Displays detailed information about a specified virtual
                  cluster. Virtual cluster is a managed entity on Amazon EMR on
                  EKS. You can create, describe, list and delete virtual
                  clusters. They do not consume any additional resource in your
                  system. A single virtual cluster maps to a single Kubernetes
                  namespace. Given this relationship, you can model virtual
                  clusters the same way you model Kubernetes namespaces to meet
                  your requirements.</p>
                tags:
                  - Describe
                  - Virtual
                  - Cluster
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
                  - Endpoints
            /virtualclusters/{virtualClusterId}/endpoints/{endpointId}/credentials:
              POST:
                summary: GetManagedEndpointSessionCredentials
                description: >-
                  <p>Generate a session token to connect to a managed endpoint.
                  </p>
                tags:
                  - Get
                  - Managed
                  - Endpoints
                  - Sessions
                  - Credentials
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
                  - Endpoints
                  - Credentials
            /virtualclusters/{virtualClusterId}/jobruns:
              POST:
                summary: StartJobRun
                description: >-
                  <p>Starts a job run. A job run is a unit of work, such as a
                  Spark jar, PySpark script, or SparkSQL query, that you submit
                  to Amazon EMR on EKS.</p>
                tags:
                  - Start
                  - Jobs
                  - Runs
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
                  - Endpoints
                  - Credentials
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from reso
                tags:
                  - Untag
                  - Resources
                  - Cluster
                  - Identifiers
                  - Job RUns
                  - Jobs
                  - Runs
                  - Job Templates
                  - Endpoints
                  - Virtual Clusters
                  - Endpoints
                  - Credentials
                  - A
    overlays:
      - type: APIs.io Search
        url: overlays/emr-containers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/emr-containers-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:emr-containers
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
  - name: finspace
    description: >-
      <p>The FinSpace management service provides the APIs for managing FinSpace
      environments.</p>
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
            title: finspace
          paths:
            /environment:
              GET:
                summary: ListEnvironments
                description: <p>A list of all of your FinSpace environments.</p>
                tags:
                  - Lists
                  - Environments
                  - Environments
            /kx/environments/{environmentId}/databases/{databaseName}/changesets:
              GET:
                summary: ListKxChangesets
                description: <p>Returns a list of all the changesets for a database.</p>
                tags:
                  - Lists
                  - Kx
                  - Change Sets
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
            /kx/environments/{environmentId}/clusters:
              GET:
                summary: ListKxClusters
                description: <p>Returns a list of clusters.</p>
                tags:
                  - Lists
                  - Kx
                  - Clusters
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
            /kx/environments/{environmentId}/databases:
              GET:
                summary: ListKxDatabases
                description: >-
                  <p>Returns a list of all the databases in the kdb
                  environment.</p>
                tags:
                  - Lists
                  - Kx
                  - Databases
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
            /kx/environments/{environmentId}/databases/{databaseName}/dataviews:
              GET:
                summary: ListKxDataviews
                description: <p> Returns a list of all the dataviews in the database.</p>
                tags:
                  - Lists
                  - Kx
                  - Data Views
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
            /kx/environments:
              GET:
                summary: ListKxEnvironments
                description: >-
                  <p>Returns a list of kdb environments created in an
                  account.</p>
                tags:
                  - Lists
                  - Kx
                  - Environments
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
            /kx/environments/{environmentId}/scalingGroups:
              GET:
                summary: ListKxScalingGroups
                description: <p> Returns a list of scaling groups in a kdb environment.</p>
                tags:
                  - Lists
                  - Kx
                  - Scaling
                  - Groups
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
            /kx/environments/{environmentId}/users:
              GET:
                summary: ListKxUsers
                description: <p>Lists all the users in a kdb environment.</p>
                tags:
                  - Lists
                  - Kx
                  - Users
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
            /kx/environments/{environmentId}/kxvolumes:
              GET:
                summary: ListKxVolumes
                description: <p> Lists all the volumes in a kdb environment. </p>
                tags:
                  - Lists
                  - Kx
                  - Volumes
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
            /environment/{environmentId}:
              PUT:
                summary: UpdateEnvironment
                description: <p>Update your FinSpace environment.</p>
                tags:
                  - Update
                  - Environments
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
            /kx/environments/{environmentId}/clusters/{clusterName}:
              GET:
                summary: GetKxCluster
                description: <p>Retrieves information about a kdb cluster.</p>
                tags:
                  - Get
                  - Kx
                  - Cluster
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
            /kx/environments/{environmentId}/databases/{databaseName}:
              PUT:
                summary: UpdateKxDatabase
                description: <p>Updates information for the given kdb database.</p>
                tags:
                  - Update
                  - Kx
                  - Databases
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
            /kx/environments/{environmentId}/databases/{databaseName}/dataviews/{dataviewName}:
              PUT:
                summary: UpdateKxDataview
                description: >-
                  <p> Updates the specified dataview. The dataviews get
                  automatically updated when any new changesets are ingested.
                  Each update of the dataview creates a new version, including
                  changeset details and cache configurations</p>
                tags:
                  - Update
                  - Kx
                  - Data Views
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
            /kx/environments/{environmentId}:
              PUT:
                summary: UpdateKxEnvironment
                description: <p>Updates information for the given kdb environment.</p>
                tags:
                  - Update
                  - Kx
                  - Environments
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
            /kx/environments/{environmentId}/scalingGroups/{scalingGroupName}:
              GET:
                summary: GetKxScalingGroup
                description: <p> Retrieves details of a scaling group.</p>
                tags:
                  - Get
                  - Kx
                  - Scaling
                  - Group
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
            /kx/environments/{environmentId}/users/{userName}:
              PUT:
                summary: UpdateKxUser
                description: >-
                  <p>Updates the user details. You can only update the IAM role
                  associated with a user.</p>
                tags:
                  - Update
                  - Kx
                  - Users
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
            /kx/environments/{environmentId}/kxvolumes/{volumeName}:
              PATCH:
                summary: UpdateKxVolume
                description: >-
                  <p> Updates the throughput or capacity of a volume. During the
                  update process, the filesystem might be unavailable for a few
                  minutes. You can retry any operations after the update is
                  complete. </p>
                tags:
                  - Update
                  - Kx
                  - Volumes
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
            /kx/environments/{environmentId}/databases/{databaseName}/changesets/{changesetId}:
              GET:
                summary: GetKxChangeset
                description: <p>Returns information about a kdb changeset.</p>
                tags:
                  - Get
                  - Kx
                  - Change Sets
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
            /kx/environments/{environmentId}/connectionString:
              GET:
                summary: GetKxConnectionString
                description: >-
                  <p>Retrieves a connection string for a user to connect to a
                  kdb cluster. You must call this API using the same role that
                  you have defined while creating a user. </p>
                tags:
                  - Get
                  - Kx
                  - Connections
                  - String
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
                  - Connections
                  - String
            /kx/environments/{environmentId}/clusters/{clusterName}/nodes:
              GET:
                summary: ListKxClusterNodes
                description: <p>Lists all the nodes in a kdb cluster.</p>
                tags:
                  - Lists
                  - Kx
                  - Cluster
                  - Nodes
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
                  - Connections
                  - String
                  - Nodes
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes metadata tags from a FinSpace resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
                  - Connections
                  - String
                  - Nodes
                  - ARN
            /kx/environments/{environmentId}/clusters/{clusterName}/configuration/code:
              PUT:
                summary: UpdateKxClusterCodeConfiguration
                description: >-
                  <p> Allows you to update code configuration on a running
                  cluster. By using this API you can update the code, the
                  initialization script path, and the command line arguments for
                  a specific cluster. The configuration that you want to update
                  will override any existing configurations on the cluster. </p>
                tags:
                  - Update
                  - Kx
                  - Cluster
                  - Code
                  - Configurations
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
                  - Connections
                  - String
                  - Nodes
                  - ARN
                  - Configurations
                  - Code
            /kx/environments/{environmentId}/clusters/{clusterName}/configuration/databases:
              PUT:
                summary: UpdateKxClusterDatabases
                description: >-
                  <p>Updates the databases mounted on a kdb cluster, which
                  includes the <code>changesetId</code> and all the dbPaths to
                  be cached. This API does not allow you to change a database
                  name or add a database if you created a cluster without one.
                  </p> <p>Using this API you can point a cluster to a different
                  changeset and modify a list of partitions being cached.</p>
                tags:
                  - Update
                  - Kx
                  - Cluster
                  - Databases
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
                  - Connections
                  - String
                  - Nodes
                  - ARN
                  - Configurations
                  - Code
            /kx/environments/{environmentId}/network:
              PUT:
                summary: UpdateKxEnvironmentNetwork
                description: >-
                  <p>Updates environment network to connect to your internal
                  network by using a transit gateway. This API supports request
                  to create a transit gateway attachment from FinSpace VPC to
                  your transit gateway ID and create a custom Route-53 outbound
                  resolvers.</p> <p>Once you send a request to update a network,
                  you cannot change it again. Network update might require
                  termination of any clusters that are running in the existing
                  ne
                tags:
                  - Update
                  - Kx
                  - Environments
                  - Networks
                  - Environments
                  - Identifiers
                  - Databases
                  - Databases
                  - Names
                  - Change Sets
                  - Clusters
                  - Data Views
                  - Kx
                  - Environments
                  - Scaling
                  - Groups
                  - Users
                  - Kxvolumes
                  - Cluster
                  - Data Views
                  - Group
                  - Users
                  - Volumes
                  - Change Sets
                  - Connections
                  - String
                  - Nodes
                  - ARN
                  - Configurations
                  - Code
                  - Networks
    overlays:
      - type: APIs.io Search
        url: overlays/finspace-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/finspace-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:finspace
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