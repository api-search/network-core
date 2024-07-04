---
name: Connections
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/connections.png
url: https://example.com/apis/connections.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Connections
apis:
  - name: apigatewaymanagementapi
    description: >-
      <p>The Amazon API Gateway Management API allows you to directly manage
      runtime aspects of your deployed APIs. To use it, you must explicitly set
      the SDK's endpoint to point to the endpoint of your deployed API. The
      endpoint will be of the form
      https://{api-id}.execute-api.{region}.amazonaws.com/{stage}, or will be
      the endpoint corresponding to your API's custom domain and base path, if
      applicable.</p>
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
            title: apigatewaymanagementapi
          paths:
            /@connections/{connectionId}:
              POST:
                summary: PostToConnection
                description: <p>Sends the provided data to the specified conne
                tags:
                  - Posts
                  - To
                  - Connections
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/apigatewaymanagementapi-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/apigatewaymanagementapi-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:apigatewaymanagementapi
  - name: apprunner
    description: >-
      <fullname>App Runner</fullname> <p>App Runner is an application service
      that provides a fast, simple, and cost-effective way to go directly from
      an existing container image or source code to a running service in the
      Amazon Web Services Cloud in seconds. You don't need to learn new
      technologies, decide which compute service to use, or understand how to
      provision and configure Amazon Web Services resources.</p> <p>App Runner
      connects directly to your container registry or source code repository. It
      provides an automatic delivery pipeline with fully managed operations,
      high performance, scalability, and security.</p> <p>For more information
      about App Runner, see the <a
      href="https://docs.aws.amazon.com/apprunner/latest/dg/">App Runner
      Developer Guide</a>. For release information, see the <a
      href="https://docs.aws.amazon.com/apprunner/latest/relnotes/">App Runner
      Release Notes</a>.</p> <p> To install the Software Development Kits
      (SDKs), Integrated Development Environment (IDE) Toolkits, and command
      line tools that you can use to access the API, see <a
      href="http://aws.amazon.com/tools/">Tools for Amazon Web Services</a>.</p>
      <p> <b>Endpoints</b> </p> <p>For a list of Region-specific endpoints that
      App Runner supports, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/apprunner.html">App
      Runner endpoints and quotas</a> in the <i>Amazon Web Services General
      Reference</i>.</p>
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
            title: apprunner
          paths:
            /:
              POST:
                summary: UpdateVpcIngressConnection
                description: >-
                  <p>Update an existing App Runner VPC Ingress Connection
                  resource. The VPC Ingress Connection must be in one of the
                  following states to be updated:</p> <ul> <li> <p> AVAILABLE
                  </p> </li> <li> <p> FAILED_CREATION </p> </li> <li> <p>
                  FAILED_UPDATE </p> <
                tags:
                  - Update
                  - VPC
                  - Ingress
                  - Connections
    overlays:
      - type: APIs.io Search
        url: overlays/apprunner-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/apprunner-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:apprunner
  - name: codeartifact
    description: >-
      <p> CodeArtifact is a fully managed artifact repository compatible with
      language-native package managers and build tools such as npm, Apache
      Maven, pip, and dotnet. You can use CodeArtifact to share packages with
      development teams and pull packages. Packages can be pulled from both
      public and CodeArtifact repositories. You can also create an upstream
      relationship between a CodeArtifact repository and another repository,
      which effectively merges their contents from the point of view of a
      package manager client. </p> <p> <b>CodeArtifact Components</b> </p>
      <p>Use the information in this guide to help you work with the following
      CodeArtifact components:</p> <ul> <li> <p> <b>Repository</b>: A
      CodeArtifact repository contains a set of <a
      href="https://docs.aws.amazon.com/codeartifact/latest/ug/welcome.html#welcome-concepts-package-version">package
      versions</a>, each of which maps to a set of assets, or files.
      Repositories are polyglot, so a single repository can contain packages of
      any supported type. Each repository exposes endpoints for fetching and
      publishing packages using tools like the <b> <code>npm</code> </b> CLI,
      the Maven CLI (<b> <code>mvn</code> </b>), Python CLIs (<b>
      <code>pip</code> </b> and <code>twine</code>), and NuGet CLIs
      (<code>nuget</code> and <code>dotnet</code>).</p> </li> <li> <p>
      <b>Domain</b>: Repositories are aggregated into a higher-level entity
      known as a <i>domain</i>. All package assets and metadata are stored in
      the domain, but are consumed through repositories. A given package asset,
      such as a Maven JAR file, is stored once per domain, no matter how many
      repositories it's present in. All of the assets and metadata in a domain
      are encrypted with the same customer master key (CMK) stored in Key
      Management Service (KMS).</p> <p>Each repository is a member of a single
      domain and can't be moved to a different domain.</p> <p>The domain allows
      organizational policy to be applied across multiple repositories, such as
      which accounts can access repositories in the domain, and which public
      repositories can be used as sources of packages.</p> <p>Although an
      organization can have multiple domains, we recommend a single production
      domain that contains all published artifacts so that teams can find and
      share packages across their organization.</p> </li> <li> <p>
      <b>Package</b>: A <i>package</i> is a bundle of software and the metadata
      required to resolve dependencies and install the software. CodeArtifact
      supports <a
      href="https://docs.aws.amazon.com/codeartifact/latest/ug/using-npm.html">npm</a>,
      <a
      href="https://docs.aws.amazon.com/codeartifact/latest/ug/using-python.html">PyPI</a>,
      <a
      href="https://docs.aws.amazon.com/codeartifact/latest/ug/using-maven">Maven</a>,
      and <a
      href="https://docs.aws.amazon.com/codeartifact/latest/ug/using-nuget">NuGet</a>
      package formats.</p> <p>In CodeArtifact, a package consists of:</p> <ul>
      <li> <p>A <i>name</i> (for example, <code>webpack</code> is the name of a
      popular npm package)</p> </li> <li> <p>An optional namespace (for example,
      <code>@types</code> in <code>@types/node</code>)</p> </li> <li> <p>A set
      of versions (for example, <code>1.0.0</code>, <code>1.0.1</code>,
      <code>1.0.2</code>, etc.)</p> </li> <li> <p> Package-level metadata (for
      example, npm tags)</p> </li> </ul> </li> <li> <p> <b>Package version</b>:
      A version of a package, such as <code>@types/node 12.6.9</code>. The
      version number format and semantics vary for different package formats.
      For example, npm package versions must conform to the <a
      href="https://semver.org/">Semantic Versioning specification</a>. In
      CodeArtifact, a package version consists of the version identifier,
      metadata at the package version level, and a set of assets.</p> </li> <li>
      <p> <b>Upstream repository</b>: One repository is <i>upstream</i> of
      another when the package versions in it can be accessed from the
      repository endpoint of the downstream repository, effectively merging the
      contents of the two repositories from the point of view of a client.
      CodeArtifact allows creating an upstream relationship between two
      repositories.</p> </li> <li> <p> <b>Asset</b>: An individual file stored
      in CodeArtifact associated with a package version, such as an npm
      <code>.tgz</code> file or Maven POM and JAR files.</p> </li> </ul>
      <p>CodeArtifact supports these operations:</p> <ul> <li> <p>
      <code>AssociateExternalConnection</code>: Adds an existing external
      connection to a repository. </p> </li> <li> <p>
      <code>CopyPackageVersions</code>: Copies package versions from one
      repository to another repository in the same domain.</p> </li> <li> <p>
      <code>CreateDomain</code>: Creates a domain</p> </li> <li> <p>
      <code>CreateRepository</code>: Creates a CodeArtifact repository in a
      domain. </p> </li> <li> <p> <code>DeleteDomain</code>: Deletes a domain.
      You cannot delete a domain that contains repositories. </p> </li> <li> <p>
      <code>DeleteDomainPermissionsPolicy</code>: Deletes the resource policy
      that is set on a domain.</p> </li> <li> <p> <code>DeletePackage</code>:
      Deletes a package and all associated package versions.</p> </li> <li> <p>
      <code>DeletePackageVersions</code>: Deletes versions of a package. After a
      package has been deleted, it can be republished, but its assets and
      metadata cannot be restored because they have been permanently removed
      from storage.</p> </li> <li> <p> <code>DeleteRepository</code>: Deletes a
      repository. </p> </li> <li> <p>
      <code>DeleteRepositoryPermissionsPolicy</code>: Deletes the resource
      policy that is set on a repository.</p> </li> <li> <p>
      <code>DescribeDomain</code>: Returns a <code>DomainDescription</code>
      object that contains information about the requested domain.</p> </li>
      <li> <p> <code>DescribePackage</code>: Returns a <a
      href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageDescription.html">PackageDescription</a>
      object that contains details about a package. </p> </li> <li> <p>
      <code>DescribePackageVersion</code>: Returns a <a
      href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageVersionDescription.html">PackageVersionDescription</a>
      object that contains details about a package version. </p> </li> <li> <p>
      <code>DescribeRepository</code>: Returns a
      <code>RepositoryDescription</code> object that contains detailed
      information about the requested repository. </p> </li> <li> <p>
      <code>DisposePackageVersions</code>: Disposes versions of a package. A
      package version with the status <code>Disposed</code> cannot be restored
      because they have been permanently removed from storage.</p> </li> <li>
      <p> <code>DisassociateExternalConnection</code>: Removes an existing
      external connection from a repository. </p> </li> <li> <p>
      <code>GetAuthorizationToken</code>: Generates a temporary authorization
      token for accessing repositories in the domain. The token expires the
      authorization period has passed. The default authorization period is 12
      hours and can be customized to any length with a maximum of 12 hours.</p>
      </li> <li> <p> <code>GetDomainPermissionsPolicy</code>: Returns the policy
      of a resource that is attached to the specified domain. </p> </li> <li>
      <p> <code>GetPackageVersionAsset</code>: Returns the contents of an asset
      that is in a package version. </p> </li> <li> <p>
      <code>GetPackageVersionReadme</code>: Gets the readme file or descriptive
      text for a package version.</p> </li> <li> <p>
      <code>GetRepositoryEndpoint</code>: Returns the endpoint of a repository
      for a specific package format. A repository has one endpoint for each
      package format: </p> <ul> <li> <p> <code>maven</code> </p> </li> <li> <p>
      <code>npm</code> </p> </li> <li> <p> <code>nuget</code> </p> </li> <li>
      <p> <code>pypi</code> </p> </li> </ul> </li> <li> <p>
      <code>GetRepositoryPermissionsPolicy</code>: Returns the resource policy
      that is set on a repository. </p> </li> <li> <p> <code>ListDomains</code>:
      Returns a list of <code>DomainSummary</code> objects. Each returned
      <code>DomainSummary</code> object contains information about a domain.</p>
      </li> <li> <p> <code>ListPackages</code>: Lists the packages in a
      repository.</p> </li> <li> <p> <code>ListPackageVersionAssets</code>:
      Lists the assets for a given package version.</p> </li> <li> <p>
      <code>ListPackageVersionDependencies</code>: Returns a list of the direct
      dependencies for a package version. </p> </li> <li> <p>
      <code>ListPackageVersions</code>: Returns a list of package versions for a
      specified package in a repository.</p> </li> <li> <p>
      <code>ListRepositories</code>: Returns a list of repositories owned by the
      Amazon Web Services account that called this method.</p> </li> <li> <p>
      <code>ListRepositoriesInDomain</code>: Returns a list of the repositories
      in a domain.</p> </li> <li> <p> <code>PublishPackageVersion</code>:
      Creates a new package version containing one or more assets.</p> </li>
      <li> <p> <code>PutDomainPermissionsPolicy</code>: Attaches a resource
      policy to a domain.</p> </li> <li> <p>
      <code>PutPackageOriginConfiguration</code>: Sets the package origin
      configuration for a package, which determine how new versions of the
      package can be added to a specific repository.</p> </li> <li> <p>
      <code>PutRepositoryPermissionsPolicy</code>: Sets the resource policy on a
      repository that specifies permissions to access it. </p> </li> <li> <p>
      <code>UpdatePackageVersionsStatus</code>: Updates the status of one or
      more versions of a package.</p> </li> <li> <p>
      <code>UpdateRepository</code>: Updates the properties of a repository.</p>
      </li> </ul>
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
            title: codeartifact
          paths:
            /v1/repository/external-connection:
              DELETE:
                summary: DisassociateExternalConnection
                description: >-
                  <p> Removes an existing external connection from a repository.
                  </p>
                tags:
                  - Disassociate
                  - External
                  - Connections
                  - null
                  - Repositories
                  - External
                  - Connections
            /v1/package/versions/copy:
              POST:
                summary: CopyPackageVersions
                description: >-
                  <p> Copies package versions from one repository to another
                  repository in the same domain. </p> <note> <p> You must
                  specify <code>versions</code> or
                  <code>versionRevisions</code>. You cannot specify both. </p>
                  </note>
                tags:
                  - Copy
                  - Packages
                  - Versions
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
            /v1/domain:
              GET:
                summary: DescribeDomain
                description: >-
                  <p> Returns a <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_DomainDescription.html">DomainDescription</a>
                  object that contains information about the requested domain.
                  </p>
                tags:
                  - Describe
                  - Domains
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
            /v1/repository:
              PUT:
                summary: UpdateRepository
                description: <p> Update the properties of a repository. </p>
                tags:
                  - Update
                  - Repositories
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
            /v1/domain/permissions/policy:
              PUT:
                summary: PutDomainPermissionsPolicy
                description: >-
                  <p> Sets a resource policy on a domain that specifies
                  permissions to access it. </p> <p> When you call
                  <code>PutDomainPermissionsPolicy</code>, the resource policy
                  on the domain is ignored when evaluting permissions. This
                  ensures that the owner of a domain cannot lock themselves out
                  of the domain, which would prevent them from being able to
                  update the resource policy. </p>
                tags:
                  - Put
                  - Domains
                  - Permissions
                  - Policies
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
            /v1/package:
              POST:
                summary: PutPackageOriginConfiguration
                description: >-
                  <p>Sets the package origin configuration for a package.</p>
                  <p>The package origin configuration determines how new
                  versions of a package can be added to a repository. You can
                  allow or block direct publishing of new package versions, or
                  ingestion and retaining of new package versions from an
                  external connection or upstream source. For more information
                  about package origin controls and configuration, see <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/ug/package-origin-controls.html">Editing
                  package origin controls</a> in the <i>CodeArtifact User
                  Guide</i>.</p> <p> <code>PutPackageOriginConfiguration</code>
                  can be called on a package that doesn't yet exist in the
                  repository. When called on a package that does not exist, a
                  package is created in the repository with no versions and the
                  requested restrictions are set on the package. This can be
                  used to preemptively block ingesting or retaining any versions
                  from external connections or upstream repositories, or to
                  block publishing any versions of the package into the
                  repository before connecting any package managers or
                  publishers to the repository.</p>
                tags:
                  - Put
                  - Packages
                  - Origin
                  - Configurations
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
            /v1/package/versions/delete:
              POST:
                summary: DeletePackageVersions
                description: >-
                  <p> Deletes one or more versions of a package. A deleted
                  package version cannot be restored in your repository. If you
                  want to remove a package version from your repository and be
                  able to restore it later, set its status to
                  <code>Archived</code>. Archived packages cannot be downloaded
                  from a repository and don't show up with list package APIs
                  (for example, <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_ListPackageVersions.html">ListPackageVersions</a>),
                  but you can restore them using <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_UpdatePackageVersionsStatus.html">UpdatePackageVersionsStatus</a>.
                  </p>
                tags:
                  - Delete
                  - Packages
                  - Versions
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
            /v1/repository/permissions/policies:
              DELETE:
                summary: DeleteRepositoryPermissionsPolicy
                description: >-
                  <p> Deletes the resource policy that is set on a repository.
                  After a resource policy is deleted, the permissions allowed
                  and denied by the deleted policy are removed. The effect of
                  deleting a resource policy might not be immediate. </p>
                  <important> <p> Use
                  <code>DeleteRepositoryPermissionsPolicy</code> with caution.
                  After a policy is deleted, Amazon Web Services users, roles,
                  and accounts lose permissions to perform the repository
                  actions granted by the deleted policy. </p> </important>
                tags:
                  - Delete
                  - Repositories
                  - Permissions
                  - Policies
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
            /v1/package/version:
              GET:
                summary: DescribePackageVersion
                description: >-
                  <p> Returns a <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageVersionDescription.html">PackageVersionDescription</a>
                  object that contains information about the requested package
                  version. </p>
                tags:
                  - Describe
                  - Packages
                  - Versions
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
            /v1/package/versions/dispose:
              POST:
                summary: DisposePackageVersions
                description: >-
                  <p> Deletes the assets in package versions and sets the
                  package versions' status to <code>Disposed</code>. A disposed
                  package version cannot be restored in your repository because
                  its assets are deleted. </p> <p> To view all disposed package
                  versions in a repository, use <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_ListPackageVersions.html">ListPackageVersions</a>
                  and set the <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_ListPackageVersions.html#API_ListPackageVersions_RequestSyntax">status</a>
                  parameter to <code>Disposed</code>. </p> <p> To view
                  information about a disposed package version, use <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_DescribePackageVersion.html">DescribePackageVersion</a>.
                  </p>
                tags:
                  - Dispose
                  - Packages
                  - Versions
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
            /v1/authorization-token:
              POST:
                summary: GetAuthorizationToken
                description: >-
                  <p> Generates a temporary authorization token for accessing
                  repositories in the domain. This API requires the
                  <code>codeartifact:GetAuthorizationToken</code> and
                  <code>sts:GetServiceBearerToken</code> permissions. For more
                  information about authorization tokens, see <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/ug/tokens-authentication.html">CodeArtifact
                  authentication and tokens</a>. </p> <note> <p>CodeArtifact
                  authorization tokens are valid for a period of 12 hours when
                  created with the <code>login</code> command. You can call
                  <code>login</code> periodically to refresh the token. When you
                  create an authorization token with the
                  <code>GetAuthorizationToken</code> API, you can set a custom
                  authorization period, up to a maximum of 12 hours, with the
                  <code>durationSeconds</code> parameter.</p> <p>The
                  authorization period begins after <code>login</code> or
                  <code>GetAuthorizationToken</code> is called. If
                  <code>login</code> or <code>GetAuthorizationToken</code> is
                  called while assuming a role, the token lifetime is
                  independent of the maximum session duration of the role. For
                  example, if you call <code>sts assume-role</code> and specify
                  a session duration of 15 minutes, then generate a CodeArtifact
                  authorization token, the token will be valid for the full
                  authorization period even though this is longer than the
                  15-minute session duration.</p> <p>See <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use.html">Using
                  IAM Roles</a> for more information on controlling session
                  duration. </p> </note>
                tags:
                  - Get
                  - Authorization
                  - Tokens
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
            /v1/package/version/asset:
              GET:
                summary: GetPackageVersionAsset
                description: >-
                  <p> Returns an asset (or file) that is in a package. For
                  example, for a Maven package version, use
                  <code>GetPackageVersionAsset</code> to download a
                  <code>JAR</code> file, a <code>POM</code> file, or any other
                  assets in the package version. </p>
                tags:
                  - Get
                  - Packages
                  - Versions
                  - Assets
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
            /v1/package/version/readme:
              GET:
                summary: GetPackageVersionReadme
                description: >-
                  <p> Gets the readme file or descriptive text for a package
                  version. </p> <p> The returned text might contain formatting.
                  For example, it might contain formatting for Markdown or
                  reStructuredText. </p>
                tags:
                  - Get
                  - Packages
                  - Versions
                  - Readme
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
            /v1/repository/endpoint:
              GET:
                summary: GetRepositoryEndpoint
                description: >-
                  <p> Returns the endpoint of a repository for a specific
                  package format. A repository has one endpoint for each package
                  format: </p> <ul> <li> <p> <code>maven</code> </p> </li> <li>
                  <p> <code>npm</code> </p> </li> <li> <p> <code>nuget</code>
                  </p> </li> <li> <p> <code>pypi</code> </p> </li> </ul>
                tags:
                  - Get
                  - Repositories
                  - Endpoints
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
            /v1/repository/permissions/policy:
              PUT:
                summary: PutRepositoryPermissionsPolicy
                description: >-
                  <p> Sets the resource policy on a repository that specifies
                  permissions to access it. </p> <p> When you call
                  <code>PutRepositoryPermissionsPolicy</code>, the resource
                  policy on the repository is ignored when evaluting
                  permissions. This ensures that the owner of a repository
                  cannot lock themselves out of the repository, which would
                  prevent them from being able to update the resource policy.
                  </p>
                tags:
                  - Put
                  - Repositories
                  - Permissions
                  - Policies
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
            /v1/domains:
              POST:
                summary: ListDomains
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageVersionDescription.html">DomainSummary</a>
                  objects for all domains owned by the Amazon Web Services
                  account that makes this call. Each returned
                  <code>DomainSummary</code> object contains information about a
                  domain. </p>
                tags:
                  - Lists
                  - Domains
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
            /v1/package/version/assets:
              POST:
                summary: ListPackageVersionAssets
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_AssetSummary.html">AssetSummary</a>
                  objects for assets in a package version. </p>
                tags:
                  - Lists
                  - Packages
                  - Versions
                  - Assets
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
            /v1/package/version/dependencies:
              POST:
                summary: ListPackageVersionDependencies
                description: >-
                  <p> Returns the direct dependencies for a package version. The
                  dependencies are returned as <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageDependency.html">PackageDependency</a>
                  objects. CodeArtifact extracts the dependencies for a package
                  version from the metadata file for the package format (for
                  example, the <code>package.json</code> file for npm packages
                  and the <code>pom.xml</code> file for Maven). Any package
                  version dependencies that are not listed in the configuration
                  file are not returned. </p>
                tags:
                  - Lists
                  - Packages
                  - Versions
                  - Dependencies
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
            /v1/package/versions:
              POST:
                summary: ListPackageVersions
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageVersionSummary.html">PackageVersionSummary</a>
                  objects for package versions in a repository that match the
                  request parameters. Package versions of all statuses will be
                  returned by default when calling
                  <code>list-package-versions</code> with no
                  <code>--status</code> parameter. </p>
                tags:
                  - Lists
                  - Packages
                  - Versions
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
            /v1/packages:
              POST:
                summary: ListPackages
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_PackageSummary.html">PackageSummary</a>
                  objects for packages in a repository that match the request
                  parameters. </p>
                tags:
                  - Lists
                  - Packages
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
            /v1/repositories:
              POST:
                summary: ListRepositories
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_RepositorySummary.html">RepositorySummary</a>
                  objects. Each <code>RepositorySummary</code> contains
                  information about a repository in the specified Amazon Web
                  Services account and that matches the input parameters. </p>
                tags:
                  - Lists
                  - Repositories
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
            /v1/domain/repositories:
              POST:
                summary: ListRepositoriesInDomain
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_RepositorySummary.html">RepositorySummary</a>
                  objects. Each <code>RepositorySummary</code> contains
                  information about a repository in the specified domain and
                  that matches the input parameters. </p>
                tags:
                  - Lists
                  - Repositories
                  - In
                  - Domains
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
            /v1/tags:
              POST:
                summary: ListTagsForResource
                description: >-
                  <p>Gets information about Amazon Web Services tags for a
                  specified Amazon Resource Name (ARN) in CodeArtifact.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
                  - Tags
            /v1/package/version/publish:
              POST:
                summary: PublishPackageVersion
                description: >-
                  <p>Creates a new package version containing one or more assets
                  (or files).</p> <p>The <code>unfinished</code> flag can be
                  used to keep the package version in the
                  <code>Unfinished</code> state until all of its assets have
                  been uploaded (see <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/ug/packages-overview.html#package-version-status.html#package-version-status">Package
                  version status</a> in the <i>CodeArtifact user guide</i>). To
                  set the package version’s status to <code>Published</code>,
                  omit the <code>unfinished</code> flag when uploading the final
                  asset, or set the status using <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_UpdatePackageVersionsStatus.html">UpdatePackageVersionStatus</a>.
                  Once a package version’s status is set to
                  <code>Published</code>, it cannot change back to
                  <code>Unfinished</code>.</p> <note> <p>Only generic packages
                  can be published using this API. For more information, see <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/ug/using-generic.html">Using
                  generic packages</a> in the <i>CodeArtifact User
                  Guide</i>.</p> </note>
                tags:
                  - Publish
                  - Packages
                  - Versions
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
                  - Tags
                  - Publish
            /v1/tag:
              POST:
                summary: TagResource
                description: <p>Adds or updates tags for a resource in CodeArtifact.</p>
                tags:
                  - Tags
                  - Resources
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
                  - Tags
                  - Publish
                  - Tags
            /v1/untag:
              POST:
                summary: UntagResource
                description: <p>Removes tags from a resource in CodeArtifact.</p>
                tags:
                  - Untag
                  - Resources
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
                  - Tags
                  - Publish
                  - Tags
                  - Untag
            /v1/package/versions/update_status:
              POST:
                summary: UpdatePackageVersionsStatus
                description: >-
                  <p> Updates the status of one or more versions of a package.
                  Using <code>UpdatePackageVersionsStatus</code>, you can update
                  the status of package versions to <code>Archived</code>,
                  <code>Published</code>, or <code>Unlisted</code>. To set the
                  status of a package version to <code>Disposed</code>, use <a
                  href="https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_DisposePackageVersions.html">DisposePackageVersion
                tags:
                  - Update
                  - Packages
                  - Versions
                  - Status
                  - null
                  - Repositories
                  - External
                  - Connections
                  - Packages
                  - Versions
                  - Copy
                  - Domains
                  - Permissions
                  - Policies
                  - Delete
                  - Policies
                  - Versions
                  - Dispose
                  - Authorization
                  - Tokens
                  - Assets
                  - Readme
                  - Endpoints
                  - Domains
                  - Assets
                  - Dependencies
                  - Packages
                  - Repositories
                  - Tags
                  - Publish
                  - Tags
                  - Untag
                  - Update_stat
    overlays:
      - type: APIs.io Search
        url: overlays/codeartifact-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codeartifact-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codeartifact
  - name: connectparticipant
    description: >-
      <p>Amazon Connect is an easy-to-use omnichannel cloud contact center
      service that enables companies of any size to deliver superior customer
      service at a lower cost. Amazon Connect communications capabilities make
      it easy for companies to deliver personalized interactions across
      communication channels, including chat. </p> <p>Use the Amazon Connect
      Participant Service to manage participants (for example, agents,
      customers, and managers listening in), and to send messages and events
      within a chat contact. The APIs in the service enable the following:
      sending chat messages, attachment sharing, managing a participant's
      connection state and message events, and retrieving chat transcripts.</p>
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
            title: connectparticipant
          paths:
            /participant/complete-attachment-upload:
              POST:
                summary: CompleteAttachmentUpload
                description: >-
                  <p>Allows you to confirm that the attachment has been uploaded
                  using the pre-signed URL provided in StartAttachmentUpload
                  API. </p> <note> <p> <code>ConnectionToken</code> is used for
                  invoking this API instead of
                  <code>ParticipantToken</code>.</p> </note> <p>The Amazon
                  Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p>
                tags:
                  - Complete
                  - Attachment
                  - Uploads
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
            /participant/connection:
              POST:
                summary: CreateParticipantConnection
                description: >-
                  <p>Creates the participant's connection. </p> <note> <p>
                  <code>ParticipantToken</code> is used for invoking this API
                  instead of <code>ConnectionToken</code>.</p> </note> <p>The
                  participant token is valid for the lifetime of the participant
                  – until they are part of a contact.</p> <p>The response URL
                  for <code>WEBSOCKET</code> Type has a connect expiry timeout
                  of 100s. Clients must manually connect to the returned
                  websocket URL and subscribe to the desired topic. </p> <p>For
                  chat, you need to publish the following on the established
                  websocket connection:</p> <p>
                  <code>{"topic":"aws/subscribe","content":{"topics":["aws/chat"]}}</code>
                  </p> <p>Upon websocket URL expiry, as specified in the
                  response ConnectionExpiry parameter, clients need to call this
                  API again to obtain a new websocket URL and perform the same
                  steps as before.</p> <p> <b>Message streaming support</b>:
                  This API can also be used together with the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_StartContactStreaming.html">StartContactStreaming</a>
                  API to create a participant connection for chat contacts that
                  are not using a websocket. For more information about message
                  streaming, <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-message-streaming.html">Enable
                  real-time chat message streaming</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p> <p> <b>Feature
                  specifications</b>: For information about feature
                  specifications, such as the allowed number of open websocket
                  connections per participant, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html#feature-limits">Feature
                  specifications</a> in the <i>Amazon Connect Administrator
                  Guide</i>. </p> <note> <p>The Amazon Connect Participant
                  Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p> </note>
                tags:
                  - Create
                  - Participants
                  - Connections
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
            /participant/views/{ViewToken}:
              GET:
                summary: DescribeView
                description: <p>Retrieves the view for the specified view token.</p>
                tags:
                  - Describe
                  - View
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
            /participant/disconnect:
              POST:
                summary: DisconnectParticipant
                description: >-
                  <p>Disconnects a participant. </p> <note> <p>
                  <code>ConnectionToken</code> is used for invoking this API
                  instead of <code>ParticipantToken</code>.</p> </note> <p>The
                  Amazon Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p>
                tags:
                  - Disconnect
                  - Participants
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
                  - Disconnect
            /participant/attachment:
              POST:
                summary: GetAttachment
                description: >-
                  <p>Provides a pre-signed URL for download of a completed
                  attachment. This is an asynchronous API for use with active
                  contacts.</p> <note> <p> <code>ConnectionToken</code> is used
                  for invoking this API instead of
                  <code>ParticipantToken</code>.</p> </note> <p>The Amazon
                  Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p>
                tags:
                  - Get
                  - Attachment
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
                  - Disconnect
            /participant/transcript:
              POST:
                summary: GetTranscript
                description: >-
                  <p>Retrieves a transcript of the session, including details
                  about any attachments. For information about accessing past
                  chat contact transcripts for a persistent chat, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-persistence.html">Enable
                  persistent chat</a>. </p> <note> <p>
                  <code>ConnectionToken</code> is used for invoking this API
                  instead of <code>ParticipantToken</code>.</p> </note> <p>The
                  Amazon Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p>
                tags:
                  - Get
                  - Transcripts
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
                  - Disconnect
                  - Transcripts
            /participant/event:
              POST:
                summary: SendEvent
                description: >-
                  <p>Sends an event. </p> <note> <p>
                  <code>ConnectionToken</code> is used for invoking this API
                  instead of <code>ParticipantToken</code>.</p> </note> <p>The
                  Amazon Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p>
                tags:
                  - Send
                  - Events
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
                  - Disconnect
                  - Transcripts
                  - Events
            /participant/message:
              POST:
                summary: SendMessage
                description: >-
                  <p>Sends a message.</p> <note> <p>
                  <code>ConnectionToken</code> is used for invoking this API
                  instead of <code>ParticipantToken</code>.</p> </note> <p>The
                  Amazon Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authentication</a>.</p>
                tags:
                  - Send
                  - Messages
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
                  - Disconnect
                  - Transcripts
                  - Events
                  - Messages
            /participant/start-attachment-upload:
              POST:
                summary: StartAttachmentUpload
                description: >-
                  <p>Provides a pre-signed Amazon S3 URL in response for
                  uploading the file directly to S3.</p> <note> <p>
                  <code>ConnectionToken</code> is used for invoking this API
                  instead of <code>ParticipantToken</code>.</p> </note> <p>The
                  Amazon Connect Participant Service APIs do not use <a
                  href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
                  Version 4 authenticatio
                tags:
                  - Start
                  - Attachment
                  - Uploads
                  - Participants
                  - Complete
                  - Attachment
                  - Uploads
                  - Connections
                  - View
                  - Tokens
                  - Disconnect
                  - Transcripts
                  - Events
                  - Messages
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/connectparticipant-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connectparticipant-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connectparticipant
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
  - name: events
    description: >-
      <p>Amazon EventBridge helps you to respond to state changes in your Amazon
      Web Services resources. When your resources change state, they
      automatically send events to an event stream. You can create rules that
      match selected events in the stream and route them to targets to take
      action. You can also use rules to take action on a predetermined schedule.
      For example, you can configure rules to:</p> <ul> <li> <p>Automatically
      invoke an Lambda function to update DNS entries when an event notifies you
      that Amazon EC2 instance enters the running state.</p> </li> <li>
      <p>Direct specific API records from CloudTrail to an Amazon Kinesis data
      stream for detailed analysis of potential security or availability
      risks.</p> </li> <li> <p>Periodically invoke a built-in target to create a
      snapshot of an Amazon EBS volume.</p> </li> </ul> <p>For more information
      about the features of Amazon EventBridge, see the <a
      href="https://docs.aws.amazon.com/eventbridge/latest/userguide">Amazon
      EventBridge User Guide</a>.</p>
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
            title: events
          paths:
            /:
              POST:
                summary: UpdateConnection
                description: <p>Updates settings for a conne
                tags:
                  - Update
                  - Connections
    overlays:
      - type: APIs.io Search
        url: overlays/events-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/events-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:events
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
  - name: networkmanager
    description: >-
      <p>Amazon Web Services enables you to centrally manage your Amazon Web
      Services Cloud WAN core network and your Transit Gateway network across
      Amazon Web Services accounts, Regions, and on-premises locations.</p>
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
            title: networkmanager
          paths:
            /attachments/{attachmentId}/accept:
              POST:
                summary: AcceptAttachment
                description: >-
                  <p>Accepts a core network attachment request. </p> <p>Once the
                  attachment request is accepted by a core network owner, the
                  attachment is created and connected to a core network.</p>
                tags:
                  - Accept
                  - Attachment
                  - Identifiers
                  - Accept
            /global-networks/{globalNetworkId}/connect-peer-associations:
              GET:
                summary: GetConnectPeerAssociations
                description: >-
                  <p>Returns information about a core network Connect peer
                  associations.</p>
                tags:
                  - Get
                  - Connect
                  - Peer
                  - Associations
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
            /global-networks/{globalNetworkId}/customer-gateway-associations:
              GET:
                summary: GetCustomerGatewayAssociations
                description: >-
                  <p>Gets the association information for customer gateways that
                  are associated with devices and links in your global
                  network.</p>
                tags:
                  - Get
                  - Customers
                  - Gateway
                  - Associations
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
            /global-networks/{globalNetworkId}/link-associations:
              GET:
                summary: GetLinkAssociations
                description: >-
                  <p>Gets the link associations for a device or a link. Either
                  the device ID or the link ID must be specified.</p>
                tags:
                  - Get
                  - Link
                  - Associations
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
            /global-networks/{globalNetworkId}/transit-gateway-connect-peer-associations:
              GET:
                summary: GetTransitGatewayConnectPeerAssociations
                description: >-
                  <p>Gets information about one or more of your transit gateway
                  Connect peer associations in a global network.</p>
                tags:
                  - Get
                  - Transit
                  - Gateway
                  - Connect
                  - Peer
                  - Associations
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
            /connect-attachments:
              POST:
                summary: CreateConnectAttachment
                description: >-
                  <p>Creates a core network Connect attachment from a specified
                  core network attachment. </p> <p>A core network Connect
                  attachment is a GRE-based tunnel attachment that you can use
                  to establish a connection between a core network and an
                  appliance. A core network Connect attachment uses an existing
                  VPC attachment as the underlying transport mechanism.</p>
                tags:
                  - Create
                  - Connect
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
            /connect-peers:
              GET:
                summary: ListConnectPeers
                description: <p>Returns a list of core network Connect peers.</p>
                tags:
                  - Lists
                  - Connect
                  - Peers
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
            /global-networks/{globalNetworkId}/connections:
              GET:
                summary: GetConnections
                description: >-
                  <p>Gets information about one or more of your connections in a
                  global network.</p>
                tags:
                  - Get
                  - Connections
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
            /core-networks:
              GET:
                summary: ListCoreNetworks
                description: <p>Returns a list of owned and shared core networks.</p>
                tags:
                  - Lists
                  - Core
                  - Networks
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
            /global-networks/{globalNetworkId}/devices:
              GET:
                summary: GetDevices
                description: >-
                  <p>Gets information about one or more of your devices in a
                  global network.</p>
                tags:
                  - Get
                  - Devices
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
            /global-networks:
              GET:
                summary: DescribeGlobalNetworks
                description: >-
                  <p>Describes one or more global networks. By default, all
                  global networks are described. To describe the objects in your
                  global network, you must use the appropriate <code>Get*</code>
                  action. For example, to list the transit gateways in your
                  global network, use <a>GetTransitGatewayRegistrations</a>.</p>
                tags:
                  - Describe
                  - Global
                  - Networks
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
            /global-networks/{globalNetworkId}/links:
              GET:
                summary: GetLinks
                description: >-
                  <p>Gets information about one or more links in a specified
                  global network.</p> <p>If you specify the site ID, you cannot
                  specify the type or provider in the same request. You can
                  specify the type and provider in the same request.</p>
                tags:
                  - Get
                  - Links
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
            /global-networks/{globalNetworkId}/sites:
              GET:
                summary: GetSites
                description: >-
                  <p>Gets information about one or more of your sites in a
                  global network.</p>
                tags:
                  - Get
                  - Sites
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
            /site-to-site-vpn-attachments:
              POST:
                summary: CreateSiteToSiteVpnAttachment
                description: >-
                  <p>Creates an Amazon Web Services site-to-site VPN attachment
                  on an edge location of a core network.</p>
                tags:
                  - Create
                  - Sites
                  - To
                  - VPN
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
            /transit-gateway-peerings:
              POST:
                summary: CreateTransitGatewayPeering
                description: <p>Creates a transit gateway peering connection.</p>
                tags:
                  - Create
                  - Transit
                  - Gateway
                  - Peerings
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
            /transit-gateway-route-table-attachments:
              POST:
                summary: CreateTransitGatewayRouteTableAttachment
                description: <p>Creates a transit gateway route table attachment.</p>
                tags:
                  - Create
                  - Transit
                  - Gateway
                  - Routes
                  - Tables
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
            /vpc-attachments:
              POST:
                summary: CreateVpcAttachment
                description: >-
                  <p>Creates a VPC attachment on an edge location of a core
                  network.</p>
                tags:
                  - Create
                  - VPC
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
            /attachments/{attachmentId}:
              DELETE:
                summary: DeleteAttachment
                description: <p>Deletes an attachment. Supports all attachment types.</p>
                tags:
                  - Delete
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
            /connect-peers/{connectPeerId}:
              GET:
                summary: GetConnectPeer
                description: <p>Returns information about a core network Connect peer.</p>
                tags:
                  - Get
                  - Connect
                  - Peer
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
            /global-networks/{globalNetworkId}/connections/{connectionId}:
              PATCH:
                summary: UpdateConnection
                description: >-
                  <p>Updates the information for an existing connection. To
                  remove information for any of the parameters, specify an empty
                  string.</p>
                tags:
                  - Update
                  - Connections
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
            /core-networks/{coreNetworkId}:
              PATCH:
                summary: UpdateCoreNetwork
                description: <p>Updates the description of a core network.</p>
                tags:
                  - Update
                  - Core
                  - Networks
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
            /core-networks/{coreNetworkId}/core-network-policy-versions/{policyVersionId}:
              DELETE:
                summary: DeleteCoreNetworkPolicyVersion
                description: >-
                  <p>Deletes a policy version from a core network. You can't
                  delete the current LIVE policy.</p>
                tags:
                  - Delete
                  - Core
                  - Networks
                  - Policies
                  - Versions
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
            /global-networks/{globalNetworkId}/devices/{deviceId}:
              PATCH:
                summary: UpdateDevice
                description: >-
                  <p>Updates the details for an existing device. To remove
                  information for any of the parameters, specify an empty
                  string.</p>
                tags:
                  - Update
                  - Device
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
            /global-networks/{globalNetworkId}:
              PATCH:
                summary: UpdateGlobalNetwork
                description: >-
                  <p>Updates an existing global network. To remove information
                  for any of the parameters, specify an empty string.</p>
                tags:
                  - Update
                  - Global
                  - Networks
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
            /global-networks/{globalNetworkId}/links/{linkId}:
              PATCH:
                summary: UpdateLink
                description: >-
                  <p>Updates the details for an existing link. To remove
                  information for any of the parameters, specify an empty
                  string.</p>
                tags:
                  - Update
                  - Link
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
            /peerings/{peeringId}:
              DELETE:
                summary: DeletePeering
                description: <p>Deletes an existing peering connection.</p>
                tags:
                  - Delete
                  - Peerings
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
            /resource-policy/{resourceArn}:
              POST:
                summary: PutResourcePolicy
                description: <p>Creates or updates a resource policy.</p>
                tags:
                  - Put
                  - Resources
                  - Policies
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
            /global-networks/{globalNetworkId}/sites/{siteId}:
              PATCH:
                summary: UpdateSite
                description: >-
                  <p>Updates the information for an existing site. To remove
                  information for any of the parameters, specify an empty
                  string.</p>
                tags:
                  - Update
                  - Sites
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
            /global-networks/{globalNetworkId}/transit-gateway-registrations/{transitGatewayArn}:
              DELETE:
                summary: DeregisterTransitGateway
                description: >-
                  <p>Deregisters a transit gateway from your global network.
                  This action does not delete your transit gateway, or modify
                  any of its attachments. This action removes any customer
                  gateway associations.</p>
                tags:
                  - Deregister
                  - Transit
                  - Gateway
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
            /global-networks/{globalNetworkId}/connect-peer-associations/{connectPeerId}:
              DELETE:
                summary: DisassociateConnectPeer
                description: >-
                  <p>Disassociates a core network Connect peer from a device and
                  a link. </p>
                tags:
                  - Disassociate
                  - Connect
                  - Peer
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
            /global-networks/{globalNetworkId}/customer-gateway-associations/{customerGatewayArn}:
              DELETE:
                summary: DisassociateCustomerGateway
                description: >-
                  <p>Disassociates a customer gateway from a device and a
                  link.</p>
                tags:
                  - Disassociate
                  - Customers
                  - Gateway
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
            /global-networks/{globalNetworkId}/transit-gateway-connect-peer-associations/{transitGatewayConnectPeerArn}:
              DELETE:
                summary: DisassociateTransitGatewayConnectPeer
                description: >-
                  <p>Disassociates a transit gateway Connect peer from a device
                  and link.</p>
                tags:
                  - Disassociate
                  - Transit
                  - Gateway
                  - Connect
                  - Peer
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
            /core-networks/{coreNetworkId}/core-network-change-sets/{policyVersionId}/execute:
              POST:
                summary: ExecuteCoreNetworkChangeSet
                description: >-
                  <p>Executes a change set on your core network. Deploys changes
                  globally based on the policy submitted..</p>
                tags:
                  - Execute
                  - Core
                  - Networks
                  - Change
                  - Sets
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
            /connect-attachments/{attachmentId}:
              GET:
                summary: GetConnectAttachment
                description: >-
                  <p>Returns information about a core network Connect
                  attachment.</p>
                tags:
                  - Get
                  - Connect
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
            /core-networks/{coreNetworkId}/core-network-change-events/{policyVersionId}:
              GET:
                summary: GetCoreNetworkChangeEvents
                description: <p>Returns information about a core network change event.</p>
                tags:
                  - Get
                  - Core
                  - Networks
                  - Change
                  - Events
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
            /core-networks/{coreNetworkId}/core-network-change-sets/{policyVersionId}:
              GET:
                summary: GetCoreNetworkChangeSet
                description: >-
                  <p>Returns a change set between the LIVE core network policy
                  and a submitted policy.</p>
                tags:
                  - Get
                  - Core
                  - Networks
                  - Change
                  - Sets
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
            /core-networks/{coreNetworkId}/core-network-policy:
              POST:
                summary: PutCoreNetworkPolicy
                description: >-
                  <p>Creates a new, immutable version of a core network policy.
                  A subsequent change set is created showing the differences
                  between the LIVE policy and the submitted policy.</p>
                tags:
                  - Put
                  - Core
                  - Networks
                  - Policies
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
            /global-networks/{globalNetworkId}/network-resource-count:
              GET:
                summary: GetNetworkResourceCounts
                description: >-
                  <p>Gets the count of network resources, by resource type, for
                  the specified global network.</p>
                tags:
                  - Get
                  - Networks
                  - Resources
                  - Counts
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
            /global-networks/{globalNetworkId}/network-resource-relationships:
              GET:
                summary: GetNetworkResourceRelationships
                description: >-
                  <p>Gets the network resource relationships for the specified
                  global network.</p>
                tags:
                  - Get
                  - Networks
                  - Resources
                  - Relationships
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
            /global-networks/{globalNetworkId}/network-resources:
              GET:
                summary: GetNetworkResources
                description: >-
                  <p>Describes the network resources for the specified global
                  network.</p> <p>The results include information from the
                  corresponding Describe call for the resource, minus any
                  sensitive information such as pre-shared keys.</p>
                tags:
                  - Get
                  - Networks
                  - Resources
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
            /global-networks/{globalNetworkId}/network-routes:
              POST:
                summary: GetNetworkRoutes
                description: >-
                  <p>Gets the network routes of the specified global
                  network.</p>
                tags:
                  - Get
                  - Networks
                  - Routes
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
            /global-networks/{globalNetworkId}/network-telemetry:
              GET:
                summary: GetNetworkTelemetry
                description: >-
                  <p>Gets the network telemetry of the specified global
                  network.</p>
                tags:
                  - Get
                  - Networks
                  - Telemetry
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
            /global-networks/{globalNetworkId}/route-analyses/{routeAnalysisId}:
              GET:
                summary: GetRouteAnalysis
                description: <p>Gets information about the specified route analysis.</p>
                tags:
                  - Get
                  - Routes
                  - Analysis
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /site-to-site-vpn-attachments/{attachmentId}:
              GET:
                summary: GetSiteToSiteVpnAttachment
                description: >-
                  <p>Returns information about a site-to-site VPN
                  attachment.</p>
                tags:
                  - Get
                  - Sites
                  - To
                  - VPN
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /transit-gateway-peerings/{peeringId}:
              GET:
                summary: GetTransitGatewayPeering
                description: <p>Returns information about a transit gateway peer.</p>
                tags:
                  - Get
                  - Transit
                  - Gateway
                  - Peerings
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /global-networks/{globalNetworkId}/transit-gateway-registrations:
              POST:
                summary: RegisterTransitGateway
                description: >-
                  <p>Registers a transit gateway in your global network. Not all
                  Regions support transit gateways for global networks. For a
                  list of the supported Regions, see <a
                  href="https://docs.aws.amazon.com/network-manager/latest/tgwnm/what-are-global-networks.html#nm-available-regions">Region
                  Availability</a> in the <i>Amazon Web Services Transit
                  Gateways for Global Networks User Guide</i>. The transit
                  gateway can be in any of the supported Amazon Web Services
                  Regions, but it must be owned by the same Amazon Web Services
                  account that owns the global network. You cannot register a
                  transit gateway in more than one global network.</p>
                tags:
                  - Register
                  - Transit
                  - Gateway
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /transit-gateway-route-table-attachments/{attachmentId}:
              GET:
                summary: GetTransitGatewayRouteTableAttachment
                description: >-
                  <p>Returns information about a transit gateway route table
                  attachment.</p>
                tags:
                  - Get
                  - Transit
                  - Gateway
                  - Routes
                  - Tables
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /vpc-attachments/{attachmentId}:
              PATCH:
                summary: UpdateVpcAttachment
                description: <p>Updates a VPC attachment.</p>
                tags:
                  - Update
                  - VPC
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /attachments:
              GET:
                summary: ListAttachments
                description: <p>Returns a list of core network attachments.</p>
                tags:
                  - Lists
                  - Attachments
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /core-networks/{coreNetworkId}/core-network-policy-versions:
              GET:
                summary: ListCoreNetworkPolicyVersions
                description: <p>Returns a list of core network policy versions.</p>
                tags:
                  - Lists
                  - Core
                  - Networks
                  - Policies
                  - Versions
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
            /organizations/service-access:
              POST:
                summary: StartOrganizationServiceAccessUpdate
                description: >-
                  <p>Enables the Network Manager service for an Amazon Web
                  Services Organization. This can only be called by a management
                  account within the organization. </p>
                tags:
                  - Start
                  - Organizations
                  - Services
                  - Access
                  - Update
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
            /peerings:
              GET:
                summary: ListPeerings
                description: <p>Lists the peerings for a core network.</p>
                tags:
                  - Lists
                  - Peerings
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
            /attachments/{attachmentId}/reject:
              POST:
                summary: RejectAttachment
                description: <p>Rejects a core network attachment request.</p>
                tags:
                  - Reject
                  - Attachment
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
                  - Reject
            /core-networks/{coreNetworkId}/core-network-policy-versions/{policyVersionId}/restore:
              POST:
                summary: RestoreCoreNetworkPolicyVersion
                description: >-
                  <p>Restores a previous policy version as a new, immutable
                  version of a core network policy. A subsequent change set is
                  created showing the differences between the LIVE policy and
                  restored policy.</p>
                tags:
                  - Restore
                  - Core
                  - Networks
                  - Policies
                  - Versions
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
                  - Reject
                  - Restore
            /global-networks/{globalNetworkId}/route-analyses:
              POST:
                summary: StartRouteAnalysis
                description: >-
                  <p>Starts analyzing the routing path between the specified
                  source and destination. For more information, see <a
                  href="https://docs.aws.amazon.com/vpc/latest/tgw/route-analyzer.html">Route
                  Analyzer</a>.</p>
                tags:
                  - Start
                  - Routes
                  - Analysis
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
                  - Reject
                  - Restore
            /global-networks/{globalNetworkId}/network-resources/{resourceArn}/metadata:
              PATCH:
                summary: UpdateNetworkResourceMetadata
                description: <p>Updates the resource metadata for the specified global ne
                tags:
                  - Update
                  - Networks
                  - Resources
                  - Metadata
                  - Identifiers
                  - Accept
                  - Networks
                  - Connect
                  - Peer
                  - Associations
                  - Customers
                  - Gateway
                  - Link
                  - Transit
                  - Attachments
                  - Peers
                  - Connections
                  - Core
                  - Networks
                  - Devices
                  - Global
                  - Links
                  - Sites
                  - Sites
                  - To
                  - VPN
                  - Peerings
                  - Routes
                  - Tables
                  - VPC
                  - Connections
                  - Policies
                  - Versions
                  - Versions
                  - Device
                  - ARN
                  - Registrations
                  - Change
                  - Sets
                  - Execute
                  - Events
                  - Resources
                  - Count
                  - Relationships
                  - Resources
                  - Routes
                  - Telemetry
                  - Analysis
                  - Analysis
                  - Organizations
                  - Services
                  - Access
                  - Reject
                  - Restore
                  - Metadata
    overlays:
      - type: APIs.io Search
        url: overlays/networkmanager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/networkmanager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:networkmanager
  - name: outposts
    description: >-
      <p>Amazon Web Services Outposts is a fully managed service that extends
      Amazon Web Services infrastructure, APIs, and tools to customer premises.
      By providing local access to Amazon Web Services managed infrastructure,
      Amazon Web Services Outposts enables customers to build and run
      applications on premises using the same programming interfaces as in
      Amazon Web Services Regions, while using local compute and storage
      resources for lower latency and local data processing needs.</p>
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
            title: outposts
          paths:
            /orders/{OrderId}/cancel:
              POST:
                summary: CancelOrder
                description: <p>Cancels the specified order for an Outpost.</p>
                tags:
                  - Cancel
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
            /orders:
              POST:
                summary: CreateOrder
                description: <p>Creates an order for an Outpost.</p>
                tags:
                  - Create
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
            /outposts:
              GET:
                summary: ListOutposts
                description: >-
                  <p>Lists the Outposts for your Amazon Web Services
                  account.</p> <p>Use filters to return specific results. If you
                  specify multiple filters, the results include only the
                  resources that match all of the specified filters. For a
                  filter where you can specify multiple values, the results
                  include items that match any of the values that you specify
                  for the filter.</p>
                tags:
                  - Lists
                  - Outposts
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
            /sites:
              GET:
                summary: ListSites
                description: >-
                  <p>Lists the Outpost sites for your Amazon Web Services
                  account. Use filters to return specific results.</p> <p>Use
                  filters to return specific results. If you specify multiple
                  filters, the results include only the resources that match all
                  of the specified filters. For a filter where you can specify
                  multiple values, the results include items that match any of
                  the values that you specify for the filter.</p>
                tags:
                  - Lists
                  - Sites
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
            /outposts/{OutpostId}:
              PATCH:
                summary: UpdateOutpost
                description: <p> Updates an Outpost. </p>
                tags:
                  - Update
                  - Outposts
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
            /sites/{SiteId}:
              PATCH:
                summary: UpdateSite
                description: <p>Updates the specified site.</p>
                tags:
                  - Update
                  - Sites
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
            /catalog/item/{CatalogItemId}:
              GET:
                summary: GetCatalogItem
                description: <p>Gets information about the specified catalog item.</p>
                tags:
                  - Get
                  - Catalog
                  - Items
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
            /connections/{ConnectionId}:
              GET:
                summary: GetConnection
                description: >-
                  <note> <p> Amazon Web Services uses this action to install
                  Outpost servers.</p> </note> <p> Gets information about the
                  specified connection. </p> <p> Use CloudTrail to monitor this
                  action or Amazon Web Services managed policy for Amazon Web
                  Services Outposts to secure it. For more information, see <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/security-iam-awsmanpol.html">
                  Amazon Web Services managed policies for Amazon Web Services
                  Outposts</a> and <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/logging-using-cloudtrail.html">
                  Logging Amazon Web Services Outposts API calls with Amazon Web
                  Services CloudTrail</a> in the <i>Amazon Web Services Outposts
                  User Guide</i>. </p>
                tags:
                  - Get
                  - Connections
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
            /orders/{OrderId}:
              GET:
                summary: GetOrder
                description: <p>Gets information about the specified order.</p>
                tags:
                  - Get
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
            /outposts/{OutpostId}/instanceTypes:
              GET:
                summary: GetOutpostInstanceTypes
                description: <p>Gets the instance types for the specified Outpost.</p>
                tags:
                  - Get
                  - Outposts
                  - Instances
                  - Types
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
            /sites/{SiteId}/address:
              PUT:
                summary: UpdateSiteAddress
                description: >-
                  <p>Updates the address of the specified site.</p> <p>You can't
                  update a site address if there is an order in progress. You
                  must wait for the order to complete or cancel the order.</p>
                  <p>You can update the operating address before you place an
                  order at the site, or after all Outposts that belong to the
                  site have been deactivated.</p>
                tags:
                  - Update
                  - Sites
                  - Addresses
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
            /outposts/{OutpostId}/assets:
              GET:
                summary: ListAssets
                description: >-
                  <p>Lists the hardware assets for the specified Outpost.</p>
                  <p>Use filters to return specific results. If you specify
                  multiple filters, the results include only the resources that
                  match all of the specified filters. For a filter where you can
                  specify multiple values, the results include items that match
                  any of the values that you specify for the filter.</p>
                tags:
                  - Lists
                  - Assets
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
            /catalog/items:
              GET:
                summary: ListCatalogItems
                description: >-
                  <p>Lists the items in the catalog.</p> <p>Use filters to
                  return specific results. If you specify multiple filters, the
                  results include only the resources that match all of the
                  specified filters. For a filter where you can specify multiple
                  values, the results include items that match any of the values
                  that you specify for the filter.</p>
                tags:
                  - Lists
                  - Catalog
                  - Items
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
            /list-orders:
              GET:
                summary: ListOrders
                description: >-
                  <p>Lists the Outpost orders for your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
                  - Resources
                  - ARN
            /connections:
              POST:
                summary: StartConnection
                description: >-
                  <note> <p> Amazon Web Services uses this action to install
                  Outpost servers.</p> </note> <p> Starts the connection
                  required for Outpost server installation. </p> <p> Use
                  CloudTrail to monitor this action or Amazon Web Services
                  managed policy for Amazon Web Services Outposts to secure it.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/security-iam-awsmanpol.html">
                  Amazon Web Services managed policies for Amazon Web Services
                  Outposts</a> and <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/logging-using-cloudtrail.html">
                  Logging Amazon Web Services Outposts API calls with Amazon Web
                  Services CloudTrail</a> in the <i>Amazon Web Services Outposts
                  User Guide</i>. </p>
                tags:
                  - Start
                  - Connections
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
                  - Resources
                  - ARN
                  - Connections
            /sites/{SiteId}/rackPhysicalProperties:
              PATCH:
                summary: UpdateSiteRackPhysicalProperties
                description: >-
                  <p>Update the physical and logistical details for a rack at a
                  site. For more information about hardware requirements for
                  racks, see <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/outposts-requirements.html#checklist">Network
                  readiness checklist</a> in the Amazon Web Services Outposts
                  User Guide. </p> <p>To update a rack at a site with an order
                  of <code>IN_PROGRESS</code>, you must wait for the order to
                  complete or cancel the 
                tags:
                  - Update
                  - Sites
                  - Rack
                  - Physical
                  - Properties
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
                  - Resources
                  - ARN
                  - Connections
                  - Rack
                  - Physical
                  - Properties
    overlays:
      - type: APIs.io Search
        url: overlays/outposts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/outposts-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:outposts
  - name: quicksight
    description: >-
      <fullname>Amazon QuickSight API Reference</fullname> <p>Amazon QuickSight
      is a fully managed, serverless business intelligence service for the
      Amazon Web Services Cloud that makes it easy to extend data and insights
      to every user in your organization. This API reference contains
      documentation for a programming interface that you can use to manage
      Amazon QuickSight. </p>
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
            title: quicksight
          paths:
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/ingestions/{IngestionId}:
              GET:
                summary: DescribeIngestion
                description: <p>Describes a SPICE ingestion.</p>
                tags:
                  - Describe
                  - Ingestion
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
            /accounts/{AwsAccountId}/customizations:
              PUT:
                summary: UpdateAccountCustomization
                description: >-
                  <p>Updates Amazon QuickSight customizations for the current
                  Amazon Web Services Region. Currently, the only customization
                  that you can use is a theme.</p> <p>You can use customizations
                  for your Amazon Web Services account or, if you specify a
                  namespace, for a Amazon QuickSight namespace instead.
                  Customizations that apply to a namespace override
                  customizations that apply to an Amazon Web Services account.
                  To find out which customizations apply, use the
                  <code>DescribeAccountCustomization</code> API operation. </p>
                tags:
                  - Update
                  - Account
                  - Customizations
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
            /account/{AwsAccountId}:
              GET:
                summary: DescribeAccountSubscription
                description: >-
                  <p>Use the DescribeAccountSubscription operation to receive a
                  description of an Amazon QuickSight account's subscription. A
                  successful API call returns an <code>AccountInfo</code> object
                  that includes an account's name, subscription status,
                  authentication type, edition, and notification email
                  address.</p>
                tags:
                  - Describe
                  - Account
                  - Subscriptions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
            /accounts/{AwsAccountId}/analyses/{AnalysisId}:
              PUT:
                summary: UpdateAnalysis
                description: <p>Updates an analysis in Amazon QuickSight</p>
                tags:
                  - Update
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
            /accounts/{AwsAccountId}/dashboards/{DashboardId}:
              PUT:
                summary: UpdateDashboard
                description: >-
                  <p>Updates a dashboard in an Amazon Web Services account.</p>
                  <note> <p>Updating a Dashboard creates a new dashboard version
                  but does not immediately publish the new version. You can
                  update the published version of a dashboard by using the
                  <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_UpdateDashboardPublishedVersion.html">UpdateDashboardPublishedVersion</a>
                  </code> API operation.</p> </note>
                tags:
                  - Update
                  - Dashboard
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
            /accounts/{AwsAccountId}/data-sets:
              GET:
                summary: ListDataSets
                description: >-
                  <p>Lists all of the datasets belonging to the current Amazon
                  Web Services account in an Amazon Web Services Region.</p>
                  <p>The permissions resource is
                  <code>arn:aws:quicksight:region:aws-account-id:dataset/*</code>.</p>
                tags:
                  - Lists
                  - Data
                  - Sets
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
            /accounts/{AwsAccountId}/data-sources:
              GET:
                summary: ListDataSources
                description: >-
                  <p>Lists data sources in current Amazon Web Services Region
                  that belong to this Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Data
                  - Sources
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
            /accounts/{AwsAccountId}/folders/{FolderId}:
              PUT:
                summary: UpdateFolder
                description: <p>Updates the name of a folder.</p>
                tags:
                  - Update
                  - Folder
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
            /accounts/{AwsAccountId}/folders/{FolderId}/members/{MemberType}/{MemberId}:
              DELETE:
                summary: DeleteFolderMembership
                description: >-
                  <p>Removes an asset, such as a dashboard, analysis, or
                  dataset, from a folder.</p>
                tags:
                  - Delete
                  - Folder
                  - Membership
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups:
              GET:
                summary: ListGroups
                description: <p>Lists all user groups in Amazon QuickSight. </p>
                tags:
                  - Lists
                  - Groups
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups/{GroupName}/members/{MemberName}:
              GET:
                summary: DescribeGroupMembership
                description: >-
                  <p>Use the <code>DescribeGroupMembership</code> operation to
                  determine if a user is a member of the specified group. If the
                  user exists and is a member of the specified group, an
                  associated <code>GroupMember</code> object is returned.</p>
                tags:
                  - Describe
                  - Group
                  - Membership
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
            /accounts/{AwsAccountId}/namespaces/{Namespace}/iam-policy-assignments/:
              POST:
                summary: CreateIAMPolicyAssignment
                description: >-
                  <p>Creates an assignment with one specified IAM policy,
                  identified by its Amazon Resource Name (ARN). This policy
                  assignment is attached to the specified groups or users of
                  Amazon QuickSight. Assignment names are unique per Amazon Web
                  Services account. To avoid overwriting rules in other
                  namespaces, use assignment names that are unique.</p>
                tags:
                  - Create
                  - Policies
                  - Assignment
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
            /accounts/{AwsAccountId}:
              POST:
                summary: CreateNamespace
                description: >-
                  <p>(Enterprise edition only) Creates a new namespace for you
                  to use with Amazon QuickSight.</p> <p>A namespace allows you
                  to isolate the Amazon QuickSight users and groups that are
                  registered for that namespace. Users that access the namespace
                  can share assets only with other users or groups in the same
                  namespace. They can't see users and groups in other
                  namespaces. You can create a namespace after your Amazon Web
                  Services account is subscribed to Amazon QuickSight. The
                  namespace must be unique within the Amazon Web Services
                  account. By default, there is a limit of 100 namespaces per
                  Amazon Web Services account. To increase your limit, create a
                  ticket with Amazon Web Services Support. </p>
                tags:
                  - Create
                  - Namespaces
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/refresh-schedules:
              PUT:
                summary: UpdateRefreshSchedule
                description: <p>Updates a refresh schedule for a dataset.</p>
                tags:
                  - Update
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
            /accounts/{AwsAccountId}/namespaces/{Namespace}/roles/{Role}/members/{MemberName}:
              DELETE:
                summary: DeleteRoleMembership
                description: <p>Removes a group from a role.</p>
                tags:
                  - Delete
                  - Roles
                  - Membership
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
            /accounts/{AwsAccountId}/templates/{TemplateId}:
              PUT:
                summary: UpdateTemplate
                description: >-
                  <p>Updates a template from an existing Amazon QuickSight
                  analysis or another template.</p>
                tags:
                  - Update
                  - Templates
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
            /accounts/{AwsAccountId}/templates/{TemplateId}/aliases/{AliasName}:
              PUT:
                summary: UpdateTemplateAlias
                description: <p>Updates the template alias of a template.</p>
                tags:
                  - Update
                  - Templates
                  - Alias
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
            /accounts/{AwsAccountId}/themes/{ThemeId}:
              PUT:
                summary: UpdateTheme
                description: <p>Updates a theme.</p>
                tags:
                  - Update
                  - Theme
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
            /accounts/{AwsAccountId}/themes/{ThemeId}/aliases/{AliasName}:
              PUT:
                summary: UpdateThemeAlias
                description: <p>Updates an alias of a theme.</p>
                tags:
                  - Update
                  - Theme
                  - Alias
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
            /accounts/{AwsAccountId}/topics:
              GET:
                summary: ListTopics
                description: <p>Lists all of the topics within an account.</p>
                tags:
                  - Lists
                  - Topics
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
            /accounts/{AwsAccountId}/topics/{TopicId}/schedules:
              GET:
                summary: ListTopicRefreshSchedules
                description: <p>Lists all of the refresh schedules for a topic.</p>
                tags:
                  - Lists
                  - Topics
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
            /accounts/{AwsAccountId}/vpc-connections:
              GET:
                summary: ListVPCConnections
                description: >-
                  <p>Lists all of the VPC connections in the current set Amazon
                  Web Services Region of an Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Connections
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
            /accounts/{AwsAccountId}/data-sets/{DataSetId}:
              PUT:
                summary: UpdateDataSet
                description: >-
                  <p>Updates a dataset. This operation doesn't support datasets
                  that include uploaded files as a source. Partial updates are
                  not supported by this operation.</p>
                tags:
                  - Update
                  - Data
                  - Sets
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/refresh-properties:
              PUT:
                summary: PutDataSetRefreshProperties
                description: >-
                  <p>Creates or updates the dataset refresh properties for the
                  dataset.</p>
                tags:
                  - Put
                  - Data
                  - Sets
                  - Refresh
                  - Properties
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
            /accounts/{AwsAccountId}/data-sources/{DataSourceId}:
              PUT:
                summary: UpdateDataSource
                description: <p>Updates a data source.</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups/{GroupName}:
              PUT:
                summary: UpdateGroup
                description: <p>Changes a group description. </p>
                tags:
                  - Update
                  - Group
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
            /accounts/{AwsAccountId}/namespace/{Namespace}/iam-policy-assignments/{AssignmentName}:
              DELETE:
                summary: DeleteIAMPolicyAssignment
                description: <p>Deletes an existing IAM policy assignment.</p>
                tags:
                  - Delete
                  - Policies
                  - Assignment
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
            /accounts/{AwsAccountId}/identity-propagation-config/{Service}:
              POST:
                summary: UpdateIdentityPropagationConfig
                description: >-
                  <p>Adds or updates services and authorized targets to
                  configure what the Amazon QuickSight IAM Identity Center
                  application can access.</p> <p>This operation is only
                  supported for Amazon QuickSight accounts using IAM Identity
                  Center</p>
                tags:
                  - Update
                  - Identity
                  - Propagation
                  - Configurations
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
            /accounts/{AwsAccountId}/namespaces/{Namespace}:
              GET:
                summary: DescribeNamespace
                description: <p>Describes the current namespace.</p>
                tags:
                  - Describe
                  - Namespaces
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/refresh-schedules/{ScheduleId}:
              GET:
                summary: DescribeRefreshSchedule
                description: <p>Provides a summary of a refresh schedule.</p>
                tags:
                  - Describe
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
            /accounts/{AwsAccountId}/namespaces/{Namespace}/roles/{Role}/custom-permission:
              PUT:
                summary: UpdateRoleCustomPermission
                description: >-
                  <p>Updates the custom permissions that are associated with a
                  role.</p>
                tags:
                  - Update
                  - Roles
                  - Custom
                  - Permission
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
            /accounts/{AwsAccountId}/topics/{TopicId}:
              PUT:
                summary: UpdateTopic
                description: <p>Updates a topic.</p>
                tags:
                  - Update
                  - Topics
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
            /accounts/{AwsAccountId}/topics/{TopicId}/schedules/{DatasetId}:
              PUT:
                summary: UpdateTopicRefreshSchedule
                description: <p>Updates a topic refresh schedule.</p>
                tags:
                  - Update
                  - Topics
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users/{UserName}:
              PUT:
                summary: UpdateUser
                description: <p>Updates an Amazon QuickSight user.</p>
                tags:
                  - Update
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
            /accounts/{AwsAccountId}/namespaces/{Namespace}/user-principals/{PrincipalId}:
              DELETE:
                summary: DeleteUserByPrincipalId
                description: <p>Deletes a user identified by its principal ID. </p>
                tags:
                  - Delete
                  - Users
                  - By
                  - Principals
                  - Identifiers
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
            /accounts/{AwsAccountId}/vpc-connections/{VPCConnectionId}:
              PUT:
                summary: UpdateVPCConnection
                description: <p>Updates a VPC connection.</p>
                tags:
                  - Update
                  - Connections
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
            /accounts/{AwsAccountId}/settings:
              PUT:
                summary: UpdateAccountSettings
                description: >-
                  <p>Updates the Amazon QuickSight settings in your Amazon Web
                  Services account.</p>
                tags:
                  - Update
                  - Account
                  - Settings
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
            /accounts/{AwsAccountId}/analyses/{AnalysisId}/definition:
              GET:
                summary: DescribeAnalysisDefinition
                description: >-
                  <p>Provides a detailed description of the definition of an
                  analysis.</p> <note> <p>If you do not need to know details
                  about the content of an Analysis, for instance if you are
                  trying to check the status of a recently created or updated
                  Analysis, use the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_DescribeAnalysis.html">
                  <code>DescribeAnalysis</code> </a> instead. </p> </note>
                tags:
                  - Describe
                  - Analysis
                  - Definitions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
            /accounts/{AwsAccountId}/analyses/{AnalysisId}/permissions:
              PUT:
                summary: UpdateAnalysisPermissions
                description: <p>Updates the read and write permissions for an analysis.</p>
                tags:
                  - Update
                  - Analysis
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
            /accounts/{AwsAccountId}/asset-bundle-export-jobs/{AssetBundleExportJobId}:
              GET:
                summary: DescribeAssetBundleExportJob
                description: >-
                  <p>Describes an existing export job.</p> <p>Poll job
                  descriptions after a job starts to know the status of the job.
                  When a job succeeds, a URL is provided to download the
                  exported assets' data from. Download URLs are valid for five
                  minutes after they are generated. You can call the
                  <code>DescribeAssetBundleExportJob</code> API for a new
                  download URL as needed.</p> <p>Job descriptions are available
                  for 14 days after the job starts.</p>
                tags:
                  - Describe
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
            /accounts/{AwsAccountId}/asset-bundle-import-jobs/{AssetBundleImportJobId}:
              GET:
                summary: DescribeAssetBundleImportJob
                description: >-
                  <p>Describes an existing import job.</p> <p>Poll job
                  descriptions after starting a job to know when it has
                  succeeded or failed. Job descriptions are available for 14
                  days after job starts.</p>
                tags:
                  - Describe
                  - Assets
                  - Bundles
                  - Import
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/definition:
              GET:
                summary: DescribeDashboardDefinition
                description: >-
                  <p>Provides a detailed description of the definition of a
                  dashboard.</p> <note> <p>If you do not need to know details
                  about the content of a dashboard, for instance if you are
                  trying to check the status of a recently created or updated
                  dashboard, use the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_DescribeDashboard.html">
                  <code>DescribeDashboard</code> </a> instead. </p> </note>
                tags:
                  - Describe
                  - Dashboard
                  - Definitions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/permissions:
              PUT:
                summary: UpdateDashboardPermissions
                description: <p>Updates read and write permissions on a dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/snapshot-jobs/{SnapshotJobId}:
              GET:
                summary: DescribeDashboardSnapshotJob
                description: >-
                  <p>Describes an existing snapshot job.</p> <p>Poll job
                  descriptions after a job starts to know the status of the job.
                  For information on available status codes, see
                  <code>JobStatus</code>.</p>
                tags:
                  - Describe
                  - Dashboard
                  - Snapshots
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/snapshot-jobs/{SnapshotJobId}/result:
              GET:
                summary: DescribeDashboardSnapshotJobResult
                description: >-
                  <p>Describes the result of an existing snapshot job that has
                  finished running.</p> <p>A finished snapshot job will return a
                  <code>COMPLETED</code> or <code>FAILED</code> status when you
                  poll the job with a <code>DescribeDashboardSnapshotJob</code>
                  API call.</p> <p>If the job has not finished running, this
                  operation returns a message that says <code>Dashboard Snapshot
                  Job with id &lt;SnapshotjobId&gt; has not reached a terminal
                  state.</code>.</p>
                tags:
                  - Describe
                  - Dashboard
                  - Snapshots
                  - Jobs
                  - Results
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/permissions:
              POST:
                summary: UpdateDataSetPermissions
                description: >-
                  <p>Updates the permissions on a dataset.</p> <p>The
                  permissions resource is
                  <code>arn:aws:quicksight:region:aws-account-id:dataset/data-set-id</code>.</p>
                tags:
                  - Update
                  - Data
                  - Sets
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/data-sources/{DataSourceId}/permissions:
              POST:
                summary: UpdateDataSourcePermissions
                description: <p>Updates the permissions to a data source.</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/folders/{FolderId}/permissions:
              PUT:
                summary: UpdateFolderPermissions
                description: <p>Updates permissions of a folder.</p>
                tags:
                  - Update
                  - Folder
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/folders/{FolderId}/resolved-permissions:
              GET:
                summary: DescribeFolderResolvedPermissions
                description: >-
                  <p>Describes the folder resolved permissions. Permissions
                  consists of both folder direct permissions and the inherited
                  permissions from the ancestor folders.</p>
                tags:
                  - Describe
                  - Folder
                  - Resolved
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
            /accounts/{AwsAccountId}/namespaces/{Namespace}/iam-policy-assignments/{AssignmentName}:
              PUT:
                summary: UpdateIAMPolicyAssignment
                description: >-
                  <p>Updates an existing IAM policy assignment. This operation
                  updates only the optional parameter or parameters that are
                  specified in the request. This overwrites all of the users
                  included in <code>Identities</code>. </p>
                tags:
                  - Update
                  - Policies
                  - Assignment
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
            /accounts/{AwsAccountId}/ip-restriction:
              POST:
                summary: UpdateIpRestriction
                description: >-
                  <p>Updates the content and status of IP rules. To use this
                  operation, you must provide the entire map of rules. You can
                  use the <code>DescribeIpRestriction</code> operation to get
                  the current rule map.</p>
                tags:
                  - Update
                  - IP
                  - Restrictions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/templates/{TemplateId}/definition:
              GET:
                summary: DescribeTemplateDefinition
                description: >-
                  <p>Provides a detailed description of the definition of a
                  template.</p> <note> <p>If you do not need to know details
                  about the content of a template, for instance if you are
                  trying to check the status of a recently created or updated
                  template, use the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_DescribeTemplate.html">
                  <code>DescribeTemplate</code> </a> instead. </p> </note>
                tags:
                  - Describe
                  - Templates
                  - Definitions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/templates/{TemplateId}/permissions:
              PUT:
                summary: UpdateTemplatePermissions
                description: <p>Updates the resource permissions for a template.</p>
                tags:
                  - Update
                  - Templates
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/themes/{ThemeId}/permissions:
              PUT:
                summary: UpdateThemePermissions
                description: >-
                  <p>Updates the resource permissions for a theme. Permissions
                  apply to the action to grant or revoke permissions on, for
                  example <code>"quicksight:DescribeTheme"</code>.</p> <p>Theme
                  permissions apply in groupings. Valid groupings include the
                  following for the three levels of permissions, which are user,
                  owner, or no permissions: </p> <ul> <li> <p>User</p> <ul> <li>
                  <p> <code>"quicksight:DescribeTheme"</code> </p> </li> <li>
                  <p> <code>"quicksight:DescribeThemeAlias"</code> </p> </li>
                  <li> <p> <code>"quicksight:ListThemeAliases"</code> </p> </li>
                  <li> <p> <code>"quicksight:ListThemeVersions"</code> </p>
                  </li> </ul> </li> <li> <p>Owner</p> <ul> <li> <p>
                  <code>"quicksight:DescribeTheme"</code> </p> </li> <li> <p>
                  <code>"quicksight:DescribeThemeAlias"</code> </p> </li> <li>
                  <p> <code>"quicksight:ListThemeAliases"</code> </p> </li> <li>
                  <p> <code>"quicksight:ListThemeVersions"</code> </p> </li>
                  <li> <p> <code>"quicksight:DeleteTheme"</code> </p> </li> <li>
                  <p> <code>"quicksight:UpdateTheme"</code> </p> </li> <li> <p>
                  <code>"quicksight:CreateThemeAlias"</code> </p> </li> <li> <p>
                  <code>"quicksight:DeleteThemeAlias"</code> </p> </li> <li> <p>
                  <code>"quicksight:UpdateThemeAlias"</code> </p> </li> <li> <p>
                  <code>"quicksight:UpdateThemePermissions"</code> </p> </li>
                  <li> <p> <code>"quicksight:DescribeThemePermissions"</code>
                  </p> </li> </ul> </li> <li> <p>To specify no permissions, omit
                  the permissions list.</p> </li> </ul>
                tags:
                  - Update
                  - Theme
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/topics/{TopicId}/permissions:
              PUT:
                summary: UpdateTopicPermissions
                description: <p>Updates the permissions of a topic.</p>
                tags:
                  - Update
                  - Topics
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/topics/{TopicId}/refresh/{RefreshId}:
              GET:
                summary: DescribeTopicRefresh
                description: <p>Describes the status of a topic refresh.</p>
                tags:
                  - Describe
                  - Topics
                  - Refresh
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/embed-url/anonymous-user:
              POST:
                summary: GenerateEmbedUrlForAnonymousUser
                description: >-
                  <p>Generates an embed URL that you can use to embed an Amazon
                  QuickSight dashboard or visual in your website, without having
                  to register any reader users. Before you use this action, make
                  sure that you have configured the dashboards and
                  permissions.</p> <p>The following rules apply to the generated
                  URL:</p> <ul> <li> <p>It contains a temporary bearer token. It
                  is valid for 5 minutes after it is generated. Once redeemed
                  within this period, it cannot be re-used again.</p> </li> <li>
                  <p>The URL validity period should not be confused with the
                  actual session lifetime that can be customized using the
                  <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_GenerateEmbedUrlForAnonymousUser.html#QS-GenerateEmbedUrlForAnonymousUser-request-SessionLifetimeInMinutes">SessionLifetimeInMinutes</a>
                  </code> parameter. The resulting user session is valid for 15
                  minutes (minimum) to 10 hours (maximum). The default session
                  duration is 10 hours.</p> </li> <li> <p>You are charged only
                  when the URL is used or there is interaction with Amazon
                  QuickSight.</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics.html">Embedded
                  Analytics</a> in the <i>Amazon QuickSight User Guide</i>.</p>
                  <p>For more information about the high-level steps for
                  embedding and for an interactive demo of the ways you can
                  customize embedding, visit the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/quicksight-dev-portal.html">Amazon
                  QuickSight Developer Portal</a>.</p>
                tags:
                  - Generate
                  - Embed
                  - URL
                  - For
                  - Anonymous
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
            /accounts/{AwsAccountId}/embed-url/registered-user:
              POST:
                summary: GenerateEmbedUrlForRegisteredUser
                description: >-
                  <p>Generates an embed URL that you can use to embed an Amazon
                  QuickSight experience in your website. This action can be used
                  for any type of user registered in an Amazon QuickSight
                  account. Before you use this action, make sure that you have
                  configured the relevant Amazon QuickSight resource and
                  permissions.</p> <p>The following rules apply to the generated
                  URL:</p> <ul> <li> <p>It contains a temporary bearer token. It
                  is valid for 5 minutes after it is generated. Once redeemed
                  within this period, it cannot be re-used again.</p> </li> <li>
                  <p>The URL validity period should not be confused with the
                  actual session lifetime that can be customized using the
                  <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_GenerateEmbedUrlForRegisteredUser.html#QS-GenerateEmbedUrlForRegisteredUser-request-SessionLifetimeInMinutes">SessionLifetimeInMinutes</a>
                  </code> parameter.</p> <p>The resulting user session is valid
                  for 15 minutes (minimum) to 10 hours (maximum). The default
                  session duration is 10 hours.</p> </li> <li> <p>You are
                  charged only when the URL is used or there is interaction with
                  Amazon QuickSight.</p> </li> </ul> <p>For more information,
                  see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics.html">Embedded
                  Analytics</a> in the <i>Amazon QuickSight User Guide</i>.</p>
                  <p>For more information about the high-level steps for
                  embedding and for an interactive demo of the ways you can
                  customize embedding, visit the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/quicksight-dev-portal.html">Amazon
                  QuickSight Developer Portal</a>.</p>
                tags:
                  - Generate
                  - Embed
                  - URL
                  - For
                  - Registered
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/embed-url:
              GET:
                summary: GetDashboardEmbedUrl
                description: >-
                  <p>Generates a temporary session URL and authorization
                  code(bearer token) that you can use to embed an Amazon
                  QuickSight read-only dashboard in your website or application.
                  Before you use this command, make sure that you have
                  configured the dashboards and permissions. </p> <p>Currently,
                  you can use <code>GetDashboardEmbedURL</code> only from the
                  server, not from the user's browser. The following rules apply
                  to the generated URL:</p> <ul> <li> <p>They must be used
                  together.</p> </li> <li> <p>They can be used one time
                  only.</p> </li> <li> <p>They are valid for 5 minutes after you
                  run this command.</p> </li> <li> <p>You are charged only when
                  the URL is used or there is interaction with Amazon
                  QuickSight.</p> </li> <li> <p>The resulting user session is
                  valid for 15 minutes (default) up to 10 hours (maximum). You
                  can use the optional <code>SessionLifetimeInMinutes</code>
                  parameter to customize session duration.</p> </li> </ul>
                  <p>For more information, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics-deprecated.html">Embedding
                  Analytics Using GetDashboardEmbedUrl</a> in the <i>Amazon
                  QuickSight User Guide</i>.</p> <p>For more information about
                  the high-level steps for embedding and for an interactive demo
                  of the ways you can customize embedding, visit the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/quicksight-dev-portal.html">Amazon
                  QuickSight Developer Portal</a>.</p>
                tags:
                  - Get
                  - Dashboard
                  - Embed
                  - URL
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
            /accounts/{AwsAccountId}/session-embed-url:
              GET:
                summary: GetSessionEmbedUrl
                description: >-
                  <p>Generates a session URL and authorization code that you can
                  use to embed the Amazon Amazon QuickSight console in your web
                  server code. Use <code>GetSessionEmbedUrl</code> where you
                  want to provide an authoring portal that allows users to
                  create data sources, datasets, analyses, and dashboards. The
                  users who access an embedded Amazon QuickSight console need
                  belong to the author or admin security cohort. If you want to
                  restrict permissions to some of these features, add a custom
                  permissions profile to the user with the <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_UpdateUser.html">UpdateUser</a>
                  </code> API operation. Use <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_RegisterUser.html">RegisterUser</a>
                  </code> API operation to add a new user with a custom
                  permission profile attached. For more information, see the
                  following sections in the <i>Amazon QuickSight User
                  Guide</i>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics.html">Embedding
                  Analytics</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/customizing-permissions-to-the-quicksight-console.html">Customizing
                  Access to the Amazon QuickSight Console</a> </p> </li> </ul>
                tags:
                  - Get
                  - Sessions
                  - Embed
                  - URL
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/analyses:
              GET:
                summary: ListAnalyses
                description: >-
                  <p>Lists Amazon QuickSight analyses that exist in the
                  specified Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/asset-bundle-export-jobs:
              GET:
                summary: ListAssetBundleExportJobs
                description: >-
                  <p>Lists all asset bundle export jobs that have been taken
                  place in the last 14 days. Jobs created more than 14 days ago
                  are deleted forever and are not returned. If you are using the
                  same job ID for multiple jobs,
                  <code>ListAssetBundleExportJobs</code> only returns the most
                  recent job that uses the repeated job ID.</p>
                tags:
                  - Lists
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/asset-bundle-import-jobs:
              GET:
                summary: ListAssetBundleImportJobs
                description: >-
                  <p>Lists all asset bundle import jobs that have taken place in
                  the last 14 days. Jobs created more than 14 days ago are
                  deleted forever and are not returned. If you are using the
                  same job ID for multiple jobs,
                  <code>ListAssetBundleImportJobs</code> only returns the most
                  recent job that uses the repeated job ID.</p>
                tags:
                  - Lists
                  - Assets
                  - Bundles
                  - Import
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/versions:
              GET:
                summary: ListDashboardVersions
                description: >-
                  <p>Lists all the versions of the dashboards in the Amazon
                  QuickSight subscription.</p>
                tags:
                  - Lists
                  - Dashboard
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/dashboards:
              GET:
                summary: ListDashboards
                description: <p>Lists dashboards in an Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Dashboards
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/folders/{FolderId}/members:
              GET:
                summary: ListFolderMembers
                description: >-
                  <p>List all assets (<code>DASHBOARD</code>,
                  <code>ANALYSIS</code>, and <code>DATASET</code>) in a folder.
                  </p>
                tags:
                  - Lists
                  - Folder
                  - Members
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/folders:
              GET:
                summary: ListFolders
                description: <p>Lists all folders in an account.</p>
                tags:
                  - Lists
                  - Folders
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups/{GroupName}/members:
              GET:
                summary: ListGroupMemberships
                description: <p>Lists member users in a group.</p>
                tags:
                  - Lists
                  - Group
                  - Memberships
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/namespaces/{Namespace}/v2/iam-policy-assignments:
              GET:
                summary: ListIAMPolicyAssignments
                description: >-
                  <p>Lists the IAM policy assignments in the current Amazon
                  QuickSight account.</p>
                tags:
                  - Lists
                  - Policies
                  - Assignments
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users/{UserName}/iam-policy-assignments:
              GET:
                summary: ListIAMPolicyAssignmentsForUser
                description: >-
                  <p>Lists all of the IAM policy assignments, including the
                  Amazon Resource Names (ARNs), for the IAM policies assigned to
                  the specified user and group, or groups that the user belongs
                  to.</p>
                tags:
                  - Lists
                  - Policies
                  - Assignments
                  - For
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/identity-propagation-config:
              GET:
                summary: ListIdentityPropagationConfigs
                description: >-
                  <p>Lists all services and authorized targets that the Amazon
                  QuickSight IAM Identity Center application can access.</p>
                  <p>This operation is only supported for Amazon QuickSight
                  accounts that use IAM Identity Center.</p>
                tags:
                  - Lists
                  - Identity
                  - Propagation
                  - Configurations
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/ingestions:
              GET:
                summary: ListIngestions
                description: <p>Lists the history of SPICE ingestions for a dataset.</p>
                tags:
                  - Lists
                  - Ingestions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/namespaces:
              GET:
                summary: ListNamespaces
                description: >-
                  <p>Lists the namespaces for the specified Amazon Web Services
                  account. This operation doesn't list deleted namespaces.</p>
                tags:
                  - Lists
                  - Namespaces
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/namespaces/{Namespace}/roles/{Role}/members:
              GET:
                summary: ListRoleMemberships
                description: <p>Lists all groups that are associated with a role.</p>
                tags:
                  - Lists
                  - Roles
                  - Memberships
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /resources/{ResourceArn}/tags:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag or tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/templates/{TemplateId}/aliases:
              GET:
                summary: ListTemplateAliases
                description: <p>Lists all the aliases of a template.</p>
                tags:
                  - Lists
                  - Templates
                  - Aliases
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/templates/{TemplateId}/versions:
              GET:
                summary: ListTemplateVersions
                description: >-
                  <p>Lists all the versions of the templates in the current
                  Amazon QuickSight account.</p>
                tags:
                  - Lists
                  - Templates
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/templates:
              GET:
                summary: ListTemplates
                description: >-
                  <p>Lists all the templates in the current Amazon QuickSight
                  account.</p>
                tags:
                  - Lists
                  - Templates
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/themes/{ThemeId}/aliases:
              GET:
                summary: ListThemeAliases
                description: <p>Lists all the aliases of a theme.</p>
                tags:
                  - Lists
                  - Theme
                  - Aliases
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/themes/{ThemeId}/versions:
              GET:
                summary: ListThemeVersions
                description: >-
                  <p>Lists all the versions of the themes in the current Amazon
                  Web Services account.</p>
                tags:
                  - Lists
                  - Theme
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/themes:
              GET:
                summary: ListThemes
                description: >-
                  <p>Lists all the themes in the current Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Themes
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users/{UserName}/groups:
              GET:
                summary: ListUserGroups
                description: >-
                  <p>Lists the Amazon QuickSight groups that an Amazon
                  QuickSight user is a member of.</p>
                tags:
                  - Lists
                  - Users
                  - Groups
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users:
              POST:
                summary: RegisterUser
                description: >-
                  <p>Creates an Amazon QuickSight user whose identity is
                  associated with the Identity and Access Management (IAM)
                  identity or role specified in the request. When you register a
                  new user from the Amazon QuickSight API, Amazon QuickSight
                  generates a registration URL. The user accesses this
                  registration URL to create their account. Amazon QuickSight
                  doesn't send a registration email to users who are registered
                  from the Amazon QuickSight API. If you want new users to
                  receive a registration email, then add those users in the
                  Amazon QuickSight console. For more information on registering
                  a new user in the Amazon QuickSight console, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/managing-users.html#inviting-users">
                  Inviting users to access Amazon QuickSight</a>.</p>
                tags:
                  - Register
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/restore/analyses/{AnalysisId}:
              POST:
                summary: RestoreAnalysis
                description: <p>Restores an analysis.</p>
                tags:
                  - Restore
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
            /accounts/{AwsAccountId}/search/analyses:
              POST:
                summary: SearchAnalyses
                description: >-
                  <p>Searches for analyses that belong to the user specified in
                  the filter.</p> <note> <p>This operation is eventually
                  consistent. The results are best effort and may not reflect
                  very recent updates and changes.</p> </note>
                tags:
                  - Search
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/dashboards:
              POST:
                summary: SearchDashboards
                description: >-
                  <p>Searches for dashboards that belong to a user. </p> <note>
                  <p>This operation is eventually consistent. The results are
                  best effort and may not reflect very recent updates and
                  changes.</p> </note>
                tags:
                  - Search
                  - Dashboards
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/data-sets:
              POST:
                summary: SearchDataSets
                description: >-
                  <p>Use the <code>SearchDataSets</code> operation to search for
                  datasets that belong to an account.</p>
                tags:
                  - Search
                  - Data
                  - Sets
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/data-sources:
              POST:
                summary: SearchDataSources
                description: >-
                  <p>Use the <code>SearchDataSources</code> operation to search
                  for data sources that belong to an account.</p>
                tags:
                  - Search
                  - Data
                  - Sources
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/folders:
              POST:
                summary: SearchFolders
                description: <p>Searches the subfolders in a folder.</p>
                tags:
                  - Search
                  - Folders
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups-search:
              POST:
                summary: SearchGroups
                description: >-
                  <p>Use the <code>SearchGroups</code> operation to search
                  groups in a specified Amazon QuickSight namespace using the
                  supplied filters.</p>
                tags:
                  - Search
                  - Groups
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/asset-bundle-export-jobs/export:
              POST:
                summary: StartAssetBundleExportJob
                description: >-
                  <p>Starts an Asset Bundle export job.</p> <p>An Asset Bundle
                  export job exports specified Amazon QuickSight assets. You can
                  also choose to export any asset dependencies in the same job.
                  Export jobs run asynchronously and can be polled with a
                  <code>DescribeAssetBundleExportJob</code> API call. When a job
                  is successfully completed, a download URL that contains the
                  exported assets is returned. The URL is valid for 5 minutes
                  and can be refreshed with a
                  <code>DescribeAssetBundleExportJob</code> API call. Each
                  Amazon QuickSight account can run up to 5 export jobs
                  concurrently.</p> <p>The API caller must have the necessary
                  permissions in their IAM role to access each resource before
                  the resources can be exported.</p>
                tags:
                  - Start
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/asset-bundle-import-jobs/import:
              POST:
                summary: StartAssetBundleImportJob
                description: >-
                  <p>Starts an Asset Bundle import job.</p> <p>An Asset Bundle
                  import job imports specified Amazon QuickSight assets into an
                  Amazon QuickSight account. You can also choose to import a
                  naming prefix and specified configuration overrides. The
                  assets that are contained in the bundle file that you provide
                  are used to create or update a new or existing asset in your
                  Amazon QuickSight account. Each Amazon QuickSight account can
                  run up to 5 import jobs concurrently.</p> <p>The API caller
                  must have the necessary <code>"create"</code>,
                  <code>"describe"</code>, and <code>"update"</code> permissions
                  in their IAM role to access each resource type that is
                  contained in the bundle file before the resources can be
                  imported.</p>
                tags:
                  - Start
                  - Assets
                  - Bundles
                  - Import
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/snapshot-jobs:
              POST:
                summary: StartDashboardSnapshotJob
                description: >-
                  <p>Starts an asynchronous job that generates a dashboard
                  snapshot. You can request one of the following format
                  configurations per API call.</p> <ul> <li> <p>1 paginated
                  PDF</p> </li> <li> <p>1 Excel workbook</p> </li> <li> <p>5
                  CSVs</p> </li> </ul> <p>Poll job descriptions with a
                  <code>DescribeDashboardSnapshotJob</code> API call. Once the
                  job succeeds, use the
                  <code>DescribeDashboardSnapshotJobResult</code> API to obtain
                  the download URIs that the job generates.</p>
                tags:
                  - Start
                  - Dashboard
                  - Snapshots
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/linked-entities:
              PUT:
                summary: UpdateDashboardLinks
                description: <p>Updates the linked analyses on a dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Links
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
                  - Linked
                  - Entities
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/versions/{VersionNumber}:
              PUT:
                summary: UpdateDashboardPublishedVersion
                description: <p>Updates the published version of a dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Published
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
                  - Linked
                  - Entities
                  - Versions
                  - Numbers
            /accounts/{AwsAccountId}/public-sharing-settings:
              PUT:
                summary: UpdatePublicSharingSettings
                description: >-
                  <p>Use the <code>UpdatePublicSharingSettings</code> operation
                  to turn on or turn off the public sharing settings of an
                  Amazon QuickSight dashboard.</p> <p>To use this operation,
                  turn on session capacity pricing for your Amazon QuickSight
                  account.</p> <p>Before you can turn on public sharing on your
                  account, make sure to give public sharing permissions to an
                  administrative user in the Identity and Access Management
                  (IAM) console. For more information on using IAM with Amazon
                  QuickSight, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/security_iam_service-with-iam.html">Using
                  Amazon QuickSight with IAM</a> in the <i>Amazon QuickSight
                  User Guid
                tags:
                  - Update
                  - Public
                  - Sharing
                  - Settings
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
                  - Linked
                  - Entities
                  - Versions
                  - Numbers
                  - Public
                  - Shari
    overlays:
      - type: APIs.io Search
        url: overlays/quicksight-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/quicksight-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:quicksight
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---