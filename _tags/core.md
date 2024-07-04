---
name: Core
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/core.png
url: https://example.com/apis/core.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Core
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
                  - null
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
                  - null
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
  - name: greengrass
    description: >-
      AWS IoT Greengrass seamlessly extends AWS onto physical devices so they
      can act locally on the data they generate, while still using the cloud for
      management, analytics, and durable storage. AWS IoT Greengrass ensures
      your devices can respond quickly to local events and operate with
      intermittent connectivity. AWS IoT Greengrass minimizes the cost of
      transmitting data to the cloud by allowing you to author AWS Lambda
      functions that execute locally.
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
            title: greengrass
          paths:
            /greengrass/groups/{GroupId}/role:
              GET:
                summary: GetAssociatedRole
                description: Retrieves the role associated with a particular group.
                tags:
                  - Get
                  - Associated
                  - Roles
                  - Group
                  - Identifiers
                  - Roles
            /greengrass/servicerole:
              GET:
                summary: GetServiceRoleForAccount
                description: Retrieves the service role that is attached to your account.
                tags:
                  - Get
                  - Services
                  - Roles
                  - For
                  - Account
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
            /greengrass/definition/connectors:
              GET:
                summary: ListConnectorDefinitions
                description: Retrieves a list of connector definitions.
                tags:
                  - Lists
                  - Connectors
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
            /greengrass/definition/connectors/{ConnectorDefinitionId}/versions:
              GET:
                summary: ListConnectorDefinitionVersions
                description: >-
                  Lists the versions of a connector definition, which are
                  containers for connectors. Connectors run on the Greengrass
                  core and contain built-in integration with local
                  infrastructure, device protocols, AWS, and other cloud
                  services.
                tags:
                  - Lists
                  - Connectors
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
            /greengrass/definition/cores:
              GET:
                summary: ListCoreDefinitions
                description: Retrieves a list of core definitions.
                tags:
                  - Lists
                  - Core
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
            /greengrass/definition/cores/{CoreDefinitionId}/versions:
              GET:
                summary: ListCoreDefinitionVersions
                description: Lists the versions of a core definition.
                tags:
                  - Lists
                  - Core
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
            /greengrass/groups/{GroupId}/deployments:
              GET:
                summary: ListDeployments
                description: Returns a history of deployments for the group.
                tags:
                  - Lists
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
            /greengrass/definition/devices:
              GET:
                summary: ListDeviceDefinitions
                description: Retrieves a list of device definitions.
                tags:
                  - Lists
                  - Device
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
            /greengrass/definition/devices/{DeviceDefinitionId}/versions:
              GET:
                summary: ListDeviceDefinitionVersions
                description: Lists the versions of a device definition.
                tags:
                  - Lists
                  - Device
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
            /greengrass/definition/functions:
              GET:
                summary: ListFunctionDefinitions
                description: Retrieves a list of Lambda function definitions.
                tags:
                  - Lists
                  - Functions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
            /greengrass/definition/functions/{FunctionDefinitionId}/versions:
              GET:
                summary: ListFunctionDefinitionVersions
                description: Lists the versions of a Lambda function definition.
                tags:
                  - Lists
                  - Functions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
            /greengrass/groups:
              GET:
                summary: ListGroups
                description: Retrieves a list of groups.
                tags:
                  - Lists
                  - Groups
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
            /greengrass/groups/{GroupId}/certificateauthorities:
              GET:
                summary: ListGroupCertificateAuthorities
                description: Retrieves the current CAs for a group.
                tags:
                  - Lists
                  - Group
                  - Certificates
                  - Authorities
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
            /greengrass/groups/{GroupId}/versions:
              GET:
                summary: ListGroupVersions
                description: Lists the versions of a group.
                tags:
                  - Lists
                  - Group
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
            /greengrass/definition/loggers:
              GET:
                summary: ListLoggerDefinitions
                description: Retrieves a list of logger definitions.
                tags:
                  - Lists
                  - Loggers
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
            /greengrass/definition/loggers/{LoggerDefinitionId}/versions:
              GET:
                summary: ListLoggerDefinitionVersions
                description: Lists the versions of a logger definition.
                tags:
                  - Lists
                  - Loggers
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
            /greengrass/definition/resources:
              GET:
                summary: ListResourceDefinitions
                description: Retrieves a list of resource definitions.
                tags:
                  - Lists
                  - Resources
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
            /greengrass/definition/resources/{ResourceDefinitionId}/versions:
              GET:
                summary: ListResourceDefinitionVersions
                description: Lists the versions of a resource definition.
                tags:
                  - Lists
                  - Resources
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
            /greengrass/updates:
              POST:
                summary: CreateSoftwareUpdateJob
                description: >-
                  Creates a software update for a core or group of cores
                  (specified as an IoT thing group.) Use this to update the OTA
                  Agent as well as the Greengrass core software. It makes use of
                  the IoT Jobs feature which provides additional commands to
                  manage a Greengrass core software update job.
                tags:
                  - Create
                  - Software
                  - Update
                  - Jobs
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
            /greengrass/definition/subscriptions:
              GET:
                summary: ListSubscriptionDefinitions
                description: Retrieves a list of subscription definitions.
                tags:
                  - Lists
                  - Subscriptions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}/versions:
              GET:
                summary: ListSubscriptionDefinitionVersions
                description: Lists the versions of a subscription definition.
                tags:
                  - Lists
                  - Subscriptions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/connectors/{ConnectorDefinitionId}:
              PUT:
                summary: UpdateConnectorDefinition
                description: Updates a connector definition.
                tags:
                  - Update
                  - Connectors
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/cores/{CoreDefinitionId}:
              PUT:
                summary: UpdateCoreDefinition
                description: Updates a core definition.
                tags:
                  - Update
                  - Core
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/devices/{DeviceDefinitionId}:
              PUT:
                summary: UpdateDeviceDefinition
                description: Updates a device definition.
                tags:
                  - Update
                  - Device
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/functions/{FunctionDefinitionId}:
              PUT:
                summary: UpdateFunctionDefinition
                description: Updates a Lambda function definition.
                tags:
                  - Update
                  - Functions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/groups/{GroupId}:
              PUT:
                summary: UpdateGroup
                description: Updates a group.
                tags:
                  - Update
                  - Group
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/loggers/{LoggerDefinitionId}:
              PUT:
                summary: UpdateLoggerDefinition
                description: Updates a logger definition.
                tags:
                  - Update
                  - Loggers
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/resources/{ResourceDefinitionId}:
              PUT:
                summary: UpdateResourceDefinition
                description: Updates a resource definition.
                tags:
                  - Update
                  - Resources
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}:
              PUT:
                summary: UpdateSubscriptionDefinition
                description: Updates a subscription definition.
                tags:
                  - Update
                  - Subscriptions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/bulk/deployments/{BulkDeploymentId}/status:
              GET:
                summary: GetBulkDeploymentStatus
                description: Returns the status of a bulk deployment.
                tags:
                  - Get
                  - Bulk
                  - Deployments
                  - Status
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
            /greengrass/things/{ThingName}/connectivityInfo:
              PUT:
                summary: UpdateConnectivityInfo
                description: >-
                  Updates the connectivity information for the core. Any devices
                  that belong to the group which has this core will receive this
                  information in order to find the location of the core and
                  connect to it.
                tags:
                  - Update
                  - Connectivity
                  - Info
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
            /greengrass/definition/connectors/{ConnectorDefinitionId}/versions/{ConnectorDefinitionVersionId}:
              GET:
                summary: GetConnectorDefinitionVersion
                description: >-
                  Retrieves information about a connector definition version,
                  including the connectors that the version contains. Connectors
                  are prebuilt modules that interact with local infrastructure,
                  device protocols, AWS, and other cloud services.
                tags:
                  - Get
                  - Connectors
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/cores/{CoreDefinitionId}/versions/{CoreDefinitionVersionId}:
              GET:
                summary: GetCoreDefinitionVersion
                description: Retrieves information about a core definition version.
                tags:
                  - Get
                  - Core
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/groups/{GroupId}/deployments/{DeploymentId}/status:
              GET:
                summary: GetDeploymentStatus
                description: Returns the status of a deployment.
                tags:
                  - Get
                  - Deployments
                  - Status
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/devices/{DeviceDefinitionId}/versions/{DeviceDefinitionVersionId}:
              GET:
                summary: GetDeviceDefinitionVersion
                description: Retrieves information about a device definition version.
                tags:
                  - Get
                  - Device
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/functions/{FunctionDefinitionId}/versions/{FunctionDefinitionVersionId}:
              GET:
                summary: GetFunctionDefinitionVersion
                description: >-
                  Retrieves information about a Lambda function definition
                  version, including which Lambda functions are included in the
                  version and their configurations.
                tags:
                  - Get
                  - Functions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/groups/{GroupId}/certificateauthorities/{CertificateAuthorityId}:
              GET:
                summary: GetGroupCertificateAuthority
                description: >-
                  Retreives the CA associated with a group. Returns the public
                  key of the CA.
                tags:
                  - Get
                  - Group
                  - Certificates
                  - Authority
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
            /greengrass/groups/{GroupId}/certificateauthorities/configuration/expiry:
              PUT:
                summary: UpdateGroupCertificateConfiguration
                description: Updates the Certificate expiry time for a group.
                tags:
                  - Update
                  - Group
                  - Certificates
                  - Configurations
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/groups/{GroupId}/versions/{GroupVersionId}:
              GET:
                summary: GetGroupVersion
                description: Retrieves information about a group version.
                tags:
                  - Get
                  - Group
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/loggers/{LoggerDefinitionId}/versions/{LoggerDefinitionVersionId}:
              GET:
                summary: GetLoggerDefinitionVersion
                description: Retrieves information about a logger definition version.
                tags:
                  - Get
                  - Loggers
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/resources/{ResourceDefinitionId}/versions/{ResourceDefinitionVersionId}:
              GET:
                summary: GetResourceDefinitionVersion
                description: >-
                  Retrieves information about a resource definition version,
                  including which resources are included in the version.
                tags:
                  - Get
                  - Resources
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}/versions/{SubscriptionDefinitionVersionId}:
              GET:
                summary: GetSubscriptionDefinitionVersion
                description: Retrieves information about a subscription definition version.
                tags:
                  - Get
                  - Subscriptions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/things/{ThingName}/runtimeconfig:
              PUT:
                summary: UpdateThingRuntimeConfiguration
                description: Updates the runtime configuration of a thing.
                tags:
                  - Update
                  - Things
                  - Runtime
                  - Configurations
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
            /greengrass/bulk/deployments/{BulkDeploymentId}/detailed-reports:
              GET:
                summary: ListBulkDeploymentDetailedReports
                description: >-
                  Gets a paginated list of the deployments that have been
                  started in a bulk deployment operation, and their current
                  deployment status.
                tags:
                  - Lists
                  - Bulk
                  - Deployments
                  - Detailed
                  - Reports
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
            /greengrass/bulk/deployments:
              POST:
                summary: StartBulkDeployment
                description: >-
                  Deploys multiple groups in one operation. This action starts
                  the bulk deployment of a specified set of group versions. Each
                  group version deployment will be triggered with an adaptive
                  rate that has a fixed upper limit. We recommend that you
                  include an ''X-Amzn-Client-Token'' token in every
                  ''StartBulkDeployment'' request. These requests are idempotent
                  with respect to the token and the request parameters.
                tags:
                  - Start
                  - Bulk
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
            /tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: Remove resource tags from a Greengrass Resource.
                tags:
                  - Untag
                  - Resources
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
            /greengrass/groups/{GroupId}/deployments/$reset:
              POST:
                summary: ResetDeployments
                description: Resets a group's deployments.
                tags:
                  - Reset
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
                  - $reset
            /greengrass/bulk/deployments/{BulkDeploymentId}/$stop:
              PUT:
                summary: StopBulkDeployment
                description: >-
                  Stops the execution of a bulk deployment. This action returns
                  a status of ''Stopping'' until the deployment is stopped. You
                  cannot start a new bulk deployment while a previous deployment
                  is in the ''Stopping'' state. This action doesn't rollback
                  completed deployments or cancel pending de
                tags:
                  - Stop
                  - Bulk
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
                  - $reset
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/greengrass-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrass-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrass
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---