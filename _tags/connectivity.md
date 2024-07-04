---
name: Connectivity
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/connectivity.png
url: https://example.com/apis/connectivity.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Connectivity
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
                  - $st
    overlays:
      - type: APIs.io Search
        url: overlays/greengrass-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrass-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrass
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---