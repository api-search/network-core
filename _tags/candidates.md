---
name: Candidates
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/candidates.png
url: https://example.com/apis/candidates.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Candidates
apis:
  - name: greengrassv2
    description: >-
      <p>IoT Greengrass brings local compute, messaging, data management, sync,
      and ML inference capabilities to edge devices. This enables devices to
      collect and analyze data closer to the source of information, react
      autonomously to local events, and communicate securely with each other on
      local networks. Local devices can also communicate securely with Amazon
      Web Services IoT Core and export IoT data to the Amazon Web Services
      Cloud. IoT Greengrass developers can use Lambda functions and components
      to create and deploy applications to fleets of edge devices for local
      operation.</p> <p>IoT Greengrass Version 2 provides a new major version of
      the IoT Greengrass Core software, new APIs, and a new console. Use this
      API reference to learn how to use the IoT Greengrass V2 API operations to
      manage components, manage deployments, and core devices.</p> <p>For more
      information, see <a
      href="https://docs.aws.amazon.com/greengrass/v2/developerguide/what-is-iot-greengrass.html">What
      is IoT Greengrass?</a> in the <i>IoT Greengrass V2 Developer
      Guide</i>.</p>
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
            title: greengrassv2
          paths:
            /greengrass/servicerole:
              GET:
                summary: GetServiceRoleForAccount
                description: >-
                  <p>Gets the service role associated with IoT Greengrass for
                  your Amazon Web Services account in this Amazon Web Services
                  Region. IoT Greengrass uses this role to verify the identity
                  of client devices and manage core device connectivity
                  information. For more information, see <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/greengrass-service-role.html">Greengrass
                  service role</a> in the <i>IoT Greengrass Version 2 Developer
                  Guide</i>.</p>
                tags:
                  - Get
                  - Services
                  - Roles
                  - For
                  - Account
                  - Green Grass
                  - Service Roles
            /greengrass/v2/coreDevices/{coreDeviceThingName}/associateClientDevices:
              POST:
                summary: BatchAssociateClientDeviceWithCoreDevice
                description: >-
                  <p>Associates a list of client devices with a core device. Use
                  this API operation to specify which client devices can
                  discover a core device through cloud discovery. With cloud
                  discovery, client devices connect to IoT Greengrass to
                  retrieve associated core devices' connectivity information and
                  certificates. For more information, see <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/configure-cloud-discovery.html">Configure
                  cloud discovery</a> in the <i>IoT Greengrass V2 Developer
                  Guide</i>.</p> <note> <p>Client devices are local IoT devices
                  that connect to and communicate with an IoT Greengrass core
                  device over MQTT. You can connect client devices to a core
                  device to sync MQTT messages and data to Amazon Web Services
                  IoT Core and interact with client devices in Greengrass
                  components. For more information, see <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/interact-with-local-iot-devices.html">Interact
                  with local IoT devices</a> in the <i>IoT Greengrass V2
                  Developer Guide</i>.</p> </note>
                tags:
                  - Batches
                  - Associate
                  - Client
                  - Device
                  - With
                  - Core
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
            /greengrass/v2/coreDevices/{coreDeviceThingName}/disassociateClientDevices:
              POST:
                summary: BatchDisassociateClientDeviceFromCoreDevice
                description: >-
                  <p>Disassociates a list of client devices from a core device.
                  After you disassociate a client device from a core device, the
                  client device won't be able to use cloud discovery to retrieve
                  the core device's connectivity information and
                  certificates.</p>
                tags:
                  - Batches
                  - Disassociate
                  - Client
                  - Device
                  - From
                  - Core
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
            /greengrass/v2/deployments/{deploymentId}/cancel:
              POST:
                summary: CancelDeployment
                description: >-
                  <p>Cancels a deployment. This operation cancels the deployment
                  for devices that haven't yet received it. If a device already
                  received the deployment, this operation doesn't change
                  anything for that device.</p>
                tags:
                  - Cancel
                  - Deployments
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
            /greengrass/v2/createComponentVersion:
              POST:
                summary: CreateComponentVersion
                description: >-
                  <p>Creates a component. Components are software that run on
                  Greengrass core devices. After you develop and test a
                  component on your core device, you can use this operation to
                  upload your component to IoT Greengrass. Then, you can deploy
                  the component to other core devices.</p> <p>You can use this
                  operation to do the following:</p> <ul> <li> <p> <b>Create
                  components from recipes</b> </p> <p>Create a component from a
                  recipe, which is a file that defines the component's metadata,
                  parameters, dependencies, lifecycle, artifacts, and platform
                  capability. For more information, see <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/component-recipe-reference.html">IoT
                  Greengrass component recipe reference</a> in the <i>IoT
                  Greengrass V2 Developer Guide</i>.</p> <p>To create a
                  component from a recipe, specify <code>inlineRecipe</code>
                  when you call this operation.</p> </li> <li> <p> <b>Create
                  components from Lambda functions</b> </p> <p>Create a
                  component from an Lambda function that runs on IoT Greengrass.
                  This creates a recipe and artifacts from the Lambda function's
                  deployment package. You can use this operation to migrate
                  Lambda functions from IoT Greengrass V1 to IoT Greengrass
                  V2.</p> <p>This function only accepts Lambda functions that
                  use the following runtimes:</p> <ul> <li> <p>Python 2.7 –
                  <code>python2.7</code> </p> </li> <li> <p>Python 3.7 –
                  <code>python3.7</code> </p> </li> <li> <p>Python 3.8 –
                  <code>python3.8</code> </p> </li> <li> <p>Python 3.9 –
                  <code>python3.9</code> </p> </li> <li> <p>Java 8 –
                  <code>java8</code> </p> </li> <li> <p>Java 11 –
                  <code>java11</code> </p> </li> <li> <p>Node.js 10 –
                  <code>nodejs10.x</code> </p> </li> <li> <p>Node.js 12 –
                  <code>nodejs12.x</code> </p> </li> <li> <p>Node.js 14 –
                  <code>nodejs14.x</code> </p> </li> </ul> <p>To create a
                  component from a Lambda function, specify
                  <code>lambdaFunction</code> when you call this operation.</p>
                  <note> <p>IoT Greengrass currently supports Lambda functions
                  on only Linux core devices.</p> </note> </li> </ul>
                tags:
                  - Create
                  - Components
                  - Versions
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
            /greengrass/v2/deployments:
              GET:
                summary: ListDeployments
                description: <p>Retrieves a paginated list of deployments.</p>
                tags:
                  - Lists
                  - Deployments
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
            /greengrass/v2/components/{arn}:
              GET:
                summary: GetComponent
                description: <p>Gets the recipe for a version of a component.</p>
                tags:
                  - Get
                  - Components
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
            /greengrass/v2/coreDevices/{coreDeviceThingName}:
              GET:
                summary: GetCoreDevice
                description: >-
                  <p>Retrieves metadata for a Greengrass core device.</p> <note>
                  <p>IoT Greengrass relies on individual devices to send status
                  updates to the Amazon Web Services Cloud. If the IoT
                  Greengrass Core software isn't running on the device, or if
                  device isn't connected to the Amazon Web Services Cloud, then
                  the reported status of that device might not reflect its
                  current status. The status timestamp indicates when the device
                  status was last updated.</p> <p>Core devices send status
                  updates at the following times:</p> <ul> <li> <p>When the IoT
                  Greengrass Core software starts</p> </li> <li> <p>When the
                  core device receives a deployment from the Amazon Web Services
                  Cloud</p> </li> <li> <p>When the status of any component on
                  the core device becomes <code>BROKEN</code> </p> </li> <li>
                  <p>At a <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/greengrass-nucleus-component.html#greengrass-nucleus-component-configuration-fss">regular
                  interval that you can configure</a>, which defaults to 24
                  hours</p> </li> <li> <p>For IoT Greengrass Core v2.7.0, the
                  core device sends status updates upon local deployment and
                  cloud deployment</p> </li> </ul> </note>
                tags:
                  - Get
                  - Core
                  - Device
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
            /greengrass/v2/deployments/{deploymentId}:
              GET:
                summary: GetDeployment
                description: >-
                  <p>Gets a deployment. Deployments define the components that
                  run on Greengrass core devices.</p>
                tags:
                  - Get
                  - Deployments
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
            /greengrass/v2/components/{arn}/metadata:
              GET:
                summary: DescribeComponent
                description: <p>Retrieves metadata for a version of a component.</p>
                tags:
                  - Describe
                  - Components
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
            /greengrass/v2/components/{arn}/artifacts/{artifactName+}:
              GET:
                summary: GetComponentVersionArtifact
                description: >-
                  <p>Gets the pre-signed URL to download a public or a Lambda
                  component artifact. Core devices call this operation to
                  identify the URL that they can use to download an artifact to
                  install.</p>
                tags:
                  - Get
                  - Components
                  - Versions
                  - Artifacts
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
            /greengrass/things/{thingName}/connectivityInfo:
              PUT:
                summary: UpdateConnectivityInfo
                description: >-
                  <p>Updates connectivity information for a Greengrass core
                  device.</p> <p>Connectivity information includes endpoints and
                  ports where client devices can connect to an MQTT broker on
                  the core device. When a client device calls the <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/greengrass-discover-api.html">IoT
                  Greengrass discovery API</a>, IoT Greengrass returns
                  connectivity information for all of the core devices where the
                  client device can connect. For more information, see <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/connect-client-devices.html">Connect
                  client devices to core devices</a> in the <i>IoT Greengrass
                  Version 2 Developer Guide</i>.</p>
                tags:
                  - Update
                  - Connectivity
                  - Info
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
            /greengrass/v2/coreDevices/{coreDeviceThingName}/associatedClientDevices:
              GET:
                summary: ListClientDevicesAssociatedWithCoreDevice
                description: >-
                  <p>Retrieves a paginated list of client devices that are
                  associated with a core device.</p>
                tags:
                  - Lists
                  - Client
                  - Devices
                  - Associated
                  - With
                  - Core
                  - Device
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
            /greengrass/v2/components/{arn}/versions:
              GET:
                summary: ListComponentVersions
                description: >-
                  <p>Retrieves a paginated list of all versions for a component.
                  Greater versions are listed first.</p>
                tags:
                  - Lists
                  - Components
                  - Versions
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
            /greengrass/v2/components:
              GET:
                summary: ListComponents
                description: >-
                  <p>Retrieves a paginated list of component summaries. This
                  list includes components that you have permission to view.</p>
                tags:
                  - Lists
                  - Components
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
            /greengrass/v2/coreDevices:
              GET:
                summary: ListCoreDevices
                description: >-
                  <p>Retrieves a paginated list of Greengrass core devices.</p>
                  <note> <p>IoT Greengrass relies on individual devices to send
                  status updates to the Amazon Web Services Cloud. If the IoT
                  Greengrass Core software isn't running on the device, or if
                  device isn't connected to the Amazon Web Services Cloud, then
                  the reported status of that device might not reflect its
                  current status. The status timestamp indicates when the device
                  status was last updated.</p> <p>Core devices send status
                  updates at the following times:</p> <ul> <li> <p>When the IoT
                  Greengrass Core software starts</p> </li> <li> <p>When the
                  core device receives a deployment from the Amazon Web Services
                  Cloud</p> </li> <li> <p>When the status of any component on
                  the core device becomes <code>BROKEN</code> </p> </li> <li>
                  <p>At a <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/greengrass-nucleus-component.html#greengrass-nucleus-component-configuration-fss">regular
                  interval that you can configure</a>, which defaults to 24
                  hours</p> </li> <li> <p>For IoT Greengrass Core v2.7.0, the
                  core device sends status updates upon local deployment and
                  cloud deployment</p> </li> </ul> </note>
                tags:
                  - Lists
                  - Core
                  - Devices
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
            /greengrass/v2/coreDevices/{coreDeviceThingName}/effectiveDeployments:
              GET:
                summary: ListEffectiveDeployments
                description: >-
                  <p>Retrieves a paginated list of deployment jobs that IoT
                  Greengrass sends to Greengrass core devices.</p>
                tags:
                  - Lists
                  - Effective
                  - Deployments
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
                  - Effective
            /greengrass/v2/coreDevices/{coreDeviceThingName}/installedComponents:
              GET:
                summary: ListInstalledComponents
                description: >-
                  <p>Retrieves a paginated list of the components that a
                  Greengrass core device runs. By default, this list doesn't
                  include components that are deployed as dependencies of other
                  components. To include dependencies in the response, set the
                  <code>topologyFilter</code> parameter to <code>ALL</code>.</p>
                  <note> <p>IoT Greengrass relies on individual devices to send
                  status updates to the Amazon Web Services Cloud. If the IoT
                  Greengrass Core software isn't running on the device, or if
                  device isn't connected to the Amazon Web Services Cloud, then
                  the reported status of that device might not reflect its
                  current status. The status timestamp indicates when the device
                  status was last updated.</p> <p>Core devices send status
                  updates at the following times:</p> <ul> <li> <p>When the IoT
                  Greengrass Core software starts</p> </li> <li> <p>When the
                  core device receives a deployment from the Amazon Web Services
                  Cloud</p> </li> <li> <p>When the status of any component on
                  the core device becomes <code>BROKEN</code> </p> </li> <li>
                  <p>At a <a
                  href="https://docs.aws.amazon.com/greengrass/v2/developerguide/greengrass-nucleus-component.html#greengrass-nucleus-component-configuration-fss">regular
                  interval that you can configure</a>, which defaults to 24
                  hours</p> </li> <li> <p>For IoT Greengrass Core v2.7.0, the
                  core device sends status updates upon local deployment and
                  cloud deployment</p> </li> </ul> </note>
                tags:
                  - Lists
                  - Installed
                  - Components
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
                  - Effective
                  - Installed
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from an IoT Greengrass resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
                  - Effective
                  - Installed
            /greengrass/v2/resolveComponentCandidates:
              POST:
                summary: ResolveComponentCandidates
                description: >-
                  <p>Retrieves a list of components that meet the component,
                  version, and platform requirements of a deployment. Greengrass
                  core devices call this operation when they receive a
                  deployment to identify the components to install.</p> <p>This
                  operation identifies components that meet all dependency
                  requirements for a deployment. If the requirements conflict,
                  then this operation returns an error and the deployment fails.
                  For example, this occurs if component <code>A</code> requires
                  version <code>&gt;2.0.0</code> and component <code>B</code>
                  requires version <code>&lt;2.0.0</code> of a component
                  dependency.</p> <p>When you specify the component candidates
                  to resolve, IoT Greengrass compares each component's digest
                  from the core device with the component's digest in the Amazon
                  Web Services Cloud. If the digests don't match, then IoT
                  Greengrass specifies to use the version from the Amazon Web
                  Services Cloud.</p> <important> <p>To use this operation, you
                  must use the data plane API endpoint and authenticate with an
                  IoT device certificate. For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/greengrass.html">IoT
                  Greengrass endpoints and quotas</a>.</p> </
                tags:
                  - Resolve
                  - Components
                  - Candidates
                  - Green Grass
                  - Service Roles
                  - Devices
                  - Core
                  - Device
                  - Things
                  - Names
                  - Associate
                  - Client
                  - Disassociate
                  - Identifiers
                  - Cancel
                  - Components
                  - Versions
                  - V2
                  - Deployments
                  - Components
                  - ARN
                  - Metadata
                  - Names
                  - Connectivity
                  - Info
                  - Associated
                  - Versions
                  - Effective
                  - Installed
                  - Candidates
    overlays:
      - type: APIs.io Search
        url: overlays/greengrassv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrassv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrassv2
  - name: FactSet Concordance API
    description: >-
      The FactSet Concordance API helps our users discover the respective
      FactSet Entity & People identifier for a specific entity based off of a
      list of provided corresponding attributes, such as Names, URLs, and
      Location.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-concordance-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Concordance API
          tags:
            - name: Entity Match
              description: >-
                Retrieve a list of Entity Matches and Candidates for up to 25
                names.
            - name: Entity Match - Bulk
              description: >-
                Submit a file with a large list of entity names and attributes
                and retrieve decisions once mapped.
            - name: Universes
              description: Create, View, and Manage Universes where mappings are saved.
            - name: Mappings
              description: >-
                View all Saved Mappings in a Universe or update and save
                mappings made of ClientIds and Names to FactSet Entity Ids
            - name: Snowflake
              description: >-
                The response is formatted specifically for Snowflake environment
                and not used by consumers outside of Snowflake.
            - name: People Match
              description: Retrieve a list of People Matches.
            - name: People Mapping
              description: Used to save a single People Mapping to a given universe
          paths:
            /factset-concordance/v2/entity-match:
              get:
                summary: >-
                  Get Entity Candidates and Matches for a single name and
                  attributes.
                description: >
                  Finds the best candidate entities matching the given entity
                  name. Additional attributes can be supplied to narrow the
                  search, such as State, URL, and Entity Types. <p>**Max of 1
                  Name permitted in a single GET request.** Use the POST method
                  for /entity-match to fetch up to 25 names. Otherwise, use the
                  "Entity Match - Bulk" workflow to submit larger universes of
                  names to be concorded via a file.</p><p>
                tags:
                  - Get
                  - Entity
                  - Candidates
                  - And
                  - Matches
                  - For
                  - Single
                  - Name
                  - Attributes.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
              post:
                summary: >-
                  Get a list of Entity Candidates and Matches for a requested
                  list of up to 25 names and attributes.
                description: >
                  Finds the best candidate entities matching the given entity
                  name. If a `universeId` is provided, any match for an input
                  including a `clientId` will be saved to that universe.
                  Additional attributes can be supplied to narrow the search,
                  such as State, URL, and Entity Types. Finds the best candidate
                  entities matching the given company name. Additional
                  attributes can be supplied to narrow the search.  <p>**Max of
                  25 Names inputted.** Use the "Entity Match - Bulk" workflow to
                  submit larger universes of names to be concorded via a
                  file.</p><p> Supported types of Entities in which the names
                  can match to include -
                    * Corporations, Joint Ventures, and Holding Companies
                    * Fund Managers and various Fund Types (Open-end, Closed End, Hedge, Soverign Wealth, Pension, Exchange Traded, and more).</p>
                tags:
                  - Get
                  - List
                  - Of
                  - Entity
                  - Candidates
                  - And
                  - Matches
                  - For
                  - Requested
                  - Up
                  - To
                  - '25'
                  - Names
                  - Attributes.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
            /factset-concordance/v2/entity-task:
              post:
                summary: Input a file with names and attributes, creating a taskId.
                description: >
                  Upload a Comma-Separated List file (.csv / UTF-8 encoding)
                  with a list of names and attributes and receive a `taskId`.
                  The taskId is then used for reference in the
                  */entity-task-status* and */entity-decisions* endpoints to
                  receive results once the task is successful.<p>This is the
                  first step in the overall "Bulk" workflow. Use the
                  /entity-task-status endpoint to check the status.</p> <p> A
                  universeId must be included in request. If you do not have a
                  universe created, reference the `/universe` endpoint.
                tags:
                  - Input
                  - File
                  - With
                  - Names
                  - And
                  - Attributes,
                  - Creating
                  - Task
                  - Id.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
            /factset-concordance/v2/entity-task-status:
              get:
                summary: >-
                  Gets the status of the requested taskId or all tasks for a
                  User
                description: >
                  Pulls the **status** for ALL the Entity Tasks submitted by a
                  client within the last 30 days, and related details such as
                  task duration and decision rates. Specific Tasks can also be
                  retrieved by using the _taskId_ parameter.<p>Status types
                  include -
                    * PENDING - The task has not yet started.
                    * IN_PROGRESS - The task is submitted and decisions are in progress.
                    * SUCCESS - The task was successful! Move to the /entity-decisions endpoint to retrieve decisions.
                    * FAILURE - The task failed. Reach out to FactSet Support for assistance.
                    * BAD_REQUEST - The task creation was unsuccesfull. Typically occurs with an incorrect input file format or column headers.
                    * ABORTED - The task was aborted.
                tags:
                  - Gets
                  - The
                  - Status
                  - Of
                  - Requested
                  - Task
                  - Id
                  - Or
                  - All
                  - Tasks
                  - For
                  - User
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
            /factset-concordance/v2/entity-decisions:
              get:
                summary: Get the decisions of matches for the requested taskId.
                description: >
                  Retrieves the `Decision` objects for an Entity Task (taskId).
                  The decisions do not include all candidates, but rather the
                  results of concording the requested list of names included in
                  the input file. Mapped entities will include a FactSet Entity
                  Identifier (-E). Results will be saved to the `universeId`
                  specified in the input file.
                tags:
                  - Get
                  - The
                  - Decisions
                  - Of
                  - Matches
                  - For
                  - Requested
                  - Task
                  - Id.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
            /factset-concordance/v2/universe:
              post:
                summary: Create a new universe
                description: >
                  Create a new universe that is distinct from any existing
                  universe
                tags:
                  - Create
                  - New
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
            /factset-concordance/v2/entity-universe:
              get:
                summary: Retrieve all saved mappings within a requested universe
                description: |
                  Retrieves all entity mappings within a requested universe.
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
              post:
                summary: >-
                  Retrieve all saved mappings within a requested universe or
                  large list of client ids
                description: >
                  Retrieves all entity mappings that were saved in a given
                  universe. Supports filtering by a large number of `clientId`s
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Or
                  - Large
                  - List
                  - Of
                  - Client
                  - Ids
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
            /factset-concordance/v2/people-universe:
              get:
                summary: Retrieve all saved mappings within a requested universe
                description: |
                  Retrieves all people mappings within a requested universe.
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
              post:
                summary: >-
                  Retrieve all saved mappings within a requested universe or
                  large list of client ids
                description: >
                  Retrieves all people mappings that were saved in a given
                  universe. Supports filtering by a large number of `clientId`s
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Or
                  - Large
                  - List
                  - Of
                  - Client
                  - Ids
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
            /factset-concordance/v2/update-universe:
              post:
                summary: Update metadata for an existing universe
                description: |
                  Update metadata for an existing universe
                tags:
                  - Update
                  - Metadata
                  - For
                  - An
                  - Existing
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
            /factset-concordance/v2/universes:
              get:
                summary: Fetch metadata for universes
                description: >
                  Fetch information on active universes for the current user.
                  Optionally filter for a specific universe given a `universeId`
                tags:
                  - Fetch
                  - Metadata
                  - For
                  - Universes
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
            /factset-concordance/v2/entity-universe-statistics:
              get:
                summary: Get statistics on a given universe
                description: >
                  Get the total number of mappings in a universe, as well as the
                  number of mapped, unmapped and indeterminate mappings
                tags:
                  - Get
                  - Statistics
                  - 'On'
                  - Given
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
            /factset-concordance/v2/universe-statistics:
              get:
                summary: Get statistics on a given universe
                description: >
                  Get the total number of mappings in a universe, as well as the
                  number of mapped, unmapped and indeterminate mappings
                tags:
                  - Get
                  - Statistics
                  - 'On'
                  - Given
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
            /factset-concordance/v2/entity-mapping:
              post:
                summary: Saves a single-mapping specified by the client.
                description: >
                  Saves a Concordance Mapping to the client universe. When
                  making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  clientName are required.
                tags:
                  - Saves
                  - Single-mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
            /factset-concordance/v2/people-mapping:
              post:
                summary: Saves a single-mapping specified by the client.
                description: >
                  Saves a single Concordance People Mapping to a given universe.
                  When making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  clientName are required.
                tags:
                  - Saves
                  - Single-mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
            /factset-concordance/v2/entity-mapping-delete:
              post:
                summary: Deletes mapping specified by the client.
                description: >
                  Delete a Concordance Mapping to the client universe. When
                  making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  universeId are required.
                tags:
                  - Deletes
                  - Mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
            /factset-concordance/v2/people-mapping-delete:
              post:
                summary: Deletes mapping specified by the client.
                description: >
                  Delete a Concordance Mapping to the client universe. When
                  making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  universeId are required.
                tags:
                  - Deletes
                  - Mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
            /factset-concordance/v2/snowflake-entity-match:
              post:
                summary: >-
                  Perform an entity search and return a snowflake-friendly
                  response. Up to 25 Names per request.
                description: >
                  Finds the best candidate entities matching the given company
                  name. Additional attributes can be supplied to narrow the
                  search. *This endpoint is used natively within Snowflake and
                  is not to be consumed directly by users. Reach out to your
                  FactSet Account team to learn more about Concordance in
                  Snowflake.*
                tags:
                  - Perform
                  - An
                  - Entity
                  - Search
                  - And
                  - Return
                  - Snowflake-friendly
                  - Response.
                  - Up
                  - To
                  - '25'
                  - Names
                  - Per
                  - Request.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/snowflake-entity-mapping:
              post:
                summary: Save entity mappings to a universe
                description: Manually save or update entity mappings with metadata
                tags:
                  - Save
                  - Entity
                  - Mappings
                  - To
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-match:
              get:
                summary: >-
                  Find potential people matches given a person's name.People
                  matches can be retrieved using person's name and other
                  attributes like firstname, middlename and lastname.
                description: >
                  Finds the best people candidates matching the given name.
                  <p>**Max of 1 Name permitted in a single GET request.** Use
                  the POST method for /people-match to fetch up to 25 names.
                  Otherwise, use the "People Match - Bulk" workflow to submit
                  larger universes of names to be concorded via a file.</p><p>
                tags:
                  - Find
                  - Potential
                  - People
                  - Matches
                  - Given
                  - Person's
                  - Name.
                  - Can
                  - Be
                  - Retrieved
                  - Using
                  - Name
                  - And
                  - Other
                  - Attributes
                  - Like
                  - Firstname,
                  - Middlename
                  - Lastname.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
              post:
                summary: Find potential people matches given a person's name.
                description: >
                  Finds the best candidate people matching the given people
                  names. Additional attributes can be supplied to narrow the
                  search. If a `universeId` is provided, any match for an input
                  including a `clientId` will be saved to that universe.
                tags:
                  - Find
                  - Potential
                  - People
                  - Matches
                  - Given
                  - Person's
                  - Name.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-task:
              post:
                summary: Create a People Concordance Task.
                description: >
                  The "Bulk" workflow allows the user to create a People
                  Concordance Task. Uploading of a Comma-Separated List file
                  (.csv / UTF-8 encoding) with a list of names and attributes
                  and creation of a task id is mandatory to start the process.
                     The taskId is then used for reference in the /people-task-status and /people-decisions endpoints to receive results once the task is successful.The /people-task-status endpoint is to check the status of the Tasks as per the ids.
                      A universeId must be included in request. If you do not have a universe created, reference the /universe endpoint.The bulk workflow supports a two way approach for the user.
                    **The user can use these parameters in the following ways.**
                      1.Filling all the required fields including the `personNameColumn`.(do not include `firstNameColumn`,`lastNameColumn` & `middleNameColumn`)
                      2.Filling all the required fields excluding the `personNameColumn`.(Ensure atleast the `lastNameColumn` is filled)
                tags:
                  - Create
                  - People
                  - Concordance
                  - Task.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-task-status:
              get:
                summary: Get the Status of the People Tasks.
                description: >
                  Pulls the **status** for ALL the People Tasks submitted by a
                  client within the last 30 days, and related details such as
                  task duration and decision rates. Specific Tasks can also be
                  retrieved by using the _taskId_ parameter.<p>Status types
                  include -
                    * PENDING - The task has not yet started.
                    * IN_PROGRESS - The task is submitted and decisions are in progress.
                    * SUCCESS - The task was successful! Move to the /people-decisions endpoint to retrieve decisions.
                    * FAILURE - The task failed. Reach out to FactSet Support for assistance.
                    * BAD_REQUEST - The task creation was unsuccesfull. Typically occurs with an incorrect input file format or column headers.
                    * ABORTED - The task was aborted.
                tags:
                  - Get
                  - The
                  - Status
                  - Of
                  - People
                  - Tasks.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-decisions:
              get:
                summary: Get the decisions of matches for the requested taskId.
                description: >
                  Retrieves the `Decision` objects for an People Task (taskId).
                  The decisions do not include all candidates, but rather the
                  results of concording the requested list of names included in
                  the input file. Mapped entities will include a FactSet Entity
                  Identifier (-E). Results will be saved to the `universeId`
                  specified in the input file.
                tags:
                  - Get
                  - The
                  - Decisions
                  - Of
                  - Matches
                  - For
                  - Requested
                  - Task
                  - Id.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowfla
    overlays:
      - type: APIs.io Search
        url: overlays/concordance-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/concordance-openapi-api-evangelist-ratings.yml
    aid: factset:factset-concordance-api
  - name: FactSet Private Markets API
    description: FactSet Private Markets API
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-private-markets-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-private-markets-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-private-markets-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-private-markets-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-private-markets-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-private-markets-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Private Markets API
          tags:
            - name: Financials
              description: Retrieve Private Company Financials
            - name: Non-Periodic
              description: Retrieve Private Company Reference Data.
            - name: Data Items
              description: Retrieve available Private Company fields, metrics, and ratios.
          paths:
            /factset-private-markets/v1/financials:
              get:
                summary: Returns Private Company Financials for a list of ids.
                description: |
                  Returns Private Company Financials Information.
                tags:
                  - Returns
                  - Private
                  - Company
                  - Financials
                  - For
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
              post:
                summary: Returns Private Company Financials for a list of ids.
                description: >
                  Returns a private markets financials object for the requested
                  ids.
                tags:
                  - Returns
                  - Private
                  - Company
                  - Financials
                  - For
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
            /factset-private-markets/v1/non-periodic:
              get:
                summary: Returns Private Company reference data for a list of ids.
                description: |
                  Returns Private Company reference information.
                tags:
                  - Returns
                  - Private
                  - Company
                  - Reference
                  - Data
                  - For
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
                  - Non
                  - Periodic
              post:
                summary: Returns Private Company reference data for a list of ids.
                description: >
                  Returns a private markets reference object for the requested
                  ids.
                tags:
                  - Returns
                  - Private
                  - Company
                  - Reference
                  - Data
                  - For
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
                  - Non
                  - Periodic
            /factset-private-markets/v1/fields:
              get:
                summary: Available private company fields, metrics, and ratios.
                tags:
                  - Available
                  - Private
                  - Company
                  - Fields,
                  - Metrics,
                  - And
                  - Ratios.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
                  - Non
                  - Periodic
                  - Fields
                description: >
                  Returns list of available Private Company fields that can be
                  used in the `fields` parameter of related endpoints. These are
                  related to FactSet Private Company standardized data.
            /factset-private-markets/v1/universe:
              get:
                summary: >-
                  Get Entity Candidates and Matches for a single name and
                  attributes.
                description: >
                  Finds the best candidate entities matching the given entity
                  name. Country code can also be supplied to narrow the search.
                  <p>**Max of 1 Name permitted in a single GET request.** Use
                  the POST method for /entity-match to fetch up to 25
                  names.</p><p>
                tags:
                  - Get
                  - Entity
                  - Candidates
                  - And
                  - Matches
                  - For
                  - Single
                  - Name
                  - Attributes.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
                  - Non
                  - Periodic
                  - Fields
                  - Universe
              post:
                summary: >-
                  Get a list of Entity Candidates and Matches for a requested
                  list of up to 25 names and attributes.
                description: >
                  Finds the best candidate entities matching the given entity
                  name. Country code can also be supplied to narrow the search.
                  Finds the best candidate entities matching the given company
                  name. <p>**Max of 25 Names inputted.**</p><p>
                tags:
                  - Get
                  - List
                  - Of
                  - Entity
                  - Candidates
                  - And
                  - Matches
                  - For
                  - Requested
                  - Up
                  - To
                  - '25'
                  - Names
                  - Attributes.
                  - Factset
                  - Private
                  - Markets
                  - V1
                  - Financials
                  - Non
                  - Periodic
                  - Fields
                  - Univer
    overlays:
      - type: APIs.io Search
        url: overlays/private-markets-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/private-markets-openapi-api-evangelist-ratings.yml
    aid: factset:factset-private-markets-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---