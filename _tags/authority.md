---
name: Authority
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/authority.png
url: https://example.com/apis/authority.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Authority
apis:
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
  - name: worklink
    description: >-
      <p>Amazon WorkLink is a cloud-based service that provides secure access to
      internal websites and web apps from iOS and Android phones. In a single
      step, your users, such as employees, can access internal websites as
      efficiently as they access any other public website. They enter a URL in
      their web browser, or choose a link to an internal website in an email.
      Amazon WorkLink authenticates the user's access and securely renders
      authorized internal web content in a secure rendering service in the AWS
      cloud. Amazon WorkLink doesn't download or store any internal web content
      on mobile devices.</p>
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
            title: worklink
          paths:
            /associateDomain:
              POST:
                summary: AssociateDomain
                description: <p>Specifies a domain to be associated to Amazon WorkLink.</p>
                tags:
                  - Associate
                  - Domains
                  - Domains
            /associateWebsiteAuthorizationProvider:
              POST:
                summary: AssociateWebsiteAuthorizationProvider
                description: >-
                  <p>Associates a website authorization provider with a
                  specified fleet. This is used to authorize users against
                  associated websites in the company network.</p>
                tags:
                  - Associate
                  - Websites
                  - Authorization
                  - Providers
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
            /associateWebsiteCertificateAuthority:
              POST:
                summary: AssociateWebsiteCertificateAuthority
                description: >-
                  <p>Imports the root certificate of a certificate authority
                  (CA) used to obtain TLS certificates used by associated
                  websites within the company network.</p>
                tags:
                  - Associate
                  - Websites
                  - Certificates
                  - Authority
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
            /createFleet:
              POST:
                summary: CreateFleet
                description: >-
                  <p>Creates a fleet. A fleet consists of resources and the
                  configuration that delivers associated websites to authorized
                  users who download and set up the Amazon WorkLink app.</p>
                tags:
                  - Create
                  - Fleets
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
            /deleteFleet:
              POST:
                summary: DeleteFleet
                description: >-
                  <p>Deletes a fleet. Prevents users from accessing previously
                  associated websites. </p>
                tags:
                  - Delete
                  - Fleets
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
            /describeAuditStreamConfiguration:
              POST:
                summary: DescribeAuditStreamConfiguration
                description: >-
                  <p>Describes the configuration for delivering audit streams to
                  the customer account.</p>
                tags:
                  - Describe
                  - Audit
                  - Stream
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
            /describeCompanyNetworkConfiguration:
              POST:
                summary: DescribeCompanyNetworkConfiguration
                description: >-
                  <p>Describes the networking configuration to access the
                  internal websites associated with the specified fleet.</p>
                tags:
                  - Describe
                  - Companies
                  - Networks
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
            /describeDevice:
              POST:
                summary: DescribeDevice
                description: <p>Provides information about a user's device.</p>
                tags:
                  - Describe
                  - Device
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
            /describeDevicePolicyConfiguration:
              POST:
                summary: DescribeDevicePolicyConfiguration
                description: >-
                  <p>Describes the device policy configuration for the specified
                  fleet.</p>
                tags:
                  - Describe
                  - Device
                  - Policies
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
            /describeDomain:
              POST:
                summary: DescribeDomain
                description: <p>Provides information about the domain.</p>
                tags:
                  - Describe
                  - Domains
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
            /describeFleetMetadata:
              POST:
                summary: DescribeFleetMetadata
                description: >-
                  <p>Provides basic information for the specified fleet,
                  excluding identity provider, networking, and device
                  configuration details.</p>
                tags:
                  - Describe
                  - Fleets
                  - Metadata
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
            /describeIdentityProviderConfiguration:
              POST:
                summary: DescribeIdentityProviderConfiguration
                description: >-
                  <p>Describes the identity provider configuration of the
                  specified fleet.</p>
                tags:
                  - Describe
                  - Identity
                  - Providers
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
            /describeWebsiteCertificateAuthority:
              POST:
                summary: DescribeWebsiteCertificateAuthority
                description: <p>Provides information about the certificate authority.</p>
                tags:
                  - Describe
                  - Websites
                  - Certificates
                  - Authority
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
            /disassociateDomain:
              POST:
                summary: DisassociateDomain
                description: >-
                  <p>Disassociates a domain from Amazon WorkLink. End users lose
                  the ability to access the domain with Amazon WorkLink. </p>
                tags:
                  - Disassociate
                  - Domains
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
            /disassociateWebsiteAuthorizationProvider:
              POST:
                summary: DisassociateWebsiteAuthorizationProvider
                description: >-
                  <p>Disassociates a website authorization provider from a
                  specified fleet. After the disassociation, users can't load
                  any associated websites that require this authorization
                  provider.</p>
                tags:
                  - Disassociate
                  - Websites
                  - Authorization
                  - Providers
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
            /disassociateWebsiteCertificateAuthority:
              POST:
                summary: DisassociateWebsiteCertificateAuthority
                description: <p>Removes a certificate authority (CA).</p>
                tags:
                  - Disassociate
                  - Websites
                  - Certificates
                  - Authority
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
            /listDevices:
              POST:
                summary: ListDevices
                description: >-
                  <p>Retrieves a list of devices registered with the specified
                  fleet.</p>
                tags:
                  - Lists
                  - Devices
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
            /listDomains:
              POST:
                summary: ListDomains
                description: >-
                  <p>Retrieves a list of domains associated to a specified
                  fleet.</p>
                tags:
                  - Lists
                  - Domains
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
            /listFleets:
              POST:
                summary: ListFleets
                description: >-
                  <p>Retrieves a list of fleets for the current account and
                  Region.</p>
                tags:
                  - Lists
                  - Fleets
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
            /listWebsiteAuthorizationProviders:
              POST:
                summary: ListWebsiteAuthorizationProviders
                description: >-
                  <p>Retrieves a list of website authorization providers
                  associated with a specified fleet.</p>
                tags:
                  - Lists
                  - Websites
                  - Authorization
                  - Providers
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
            /listWebsiteCertificateAuthorities:
              POST:
                summary: ListWebsiteCertificateAuthorities
                description: >-
                  <p>Retrieves a list of certificate authorities added for the
                  current account and Region.</p>
                tags:
                  - Lists
                  - Websites
                  - Certificates
                  - Authorities
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
            /restoreDomainAccess:
              POST:
                summary: RestoreDomainAccess
                description: >-
                  <p>Moves a domain to ACTIVE status if it was in the INACTIVE
                  status.</p>
                tags:
                  - Restore
                  - Domains
                  - Access
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
            /revokeDomainAccess:
              POST:
                summary: RevokeDomainAccess
                description: >-
                  <p>Moves a domain to INACTIVE status if it was in the ACTIVE
                  status.</p>
                tags:
                  - Revoke
                  - Domains
                  - Access
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
            /signOutUser:
              POST:
                summary: SignOutUser
                description: >-
                  <p>Signs the user out from all of their devices. The user can
                  sign in again if they have valid credentials.</p>
                tags:
                  - Sign
                  - Out
                  - Users
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
            /updateAuditStreamConfiguration:
              POST:
                summary: UpdateAuditStreamConfiguration
                description: <p>Updates the audit stream configuration for the fleet.</p>
                tags:
                  - Update
                  - Audit
                  - Stream
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
            /updateCompanyNetworkConfiguration:
              POST:
                summary: UpdateCompanyNetworkConfiguration
                description: >-
                  <p>Updates the company network configuration for the
                  fleet.</p>
                tags:
                  - Update
                  - Companies
                  - Networks
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
            /updateDevicePolicyConfiguration:
              POST:
                summary: UpdateDevicePolicyConfiguration
                description: <p>Updates the device policy configuration for the fleet.</p>
                tags:
                  - Update
                  - Device
                  - Policies
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
            /updateDomainMetadata:
              POST:
                summary: UpdateDomainMetadata
                description: <p>Updates domain metadata, such as DisplayName.</p>
                tags:
                  - Update
                  - Domains
                  - Metadata
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
            /UpdateFleetMetadata:
              POST:
                summary: UpdateFleetMetadata
                description: <p>Updates fleet metadata, such as DisplayName.</p>
                tags:
                  - Update
                  - Fleets
                  - Metadata
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
                  - Update
            /updateIdentityProviderConfiguration:
              POST:
                summary: UpdateIdentityProviderConfiguration
                description: <p>Updates the identity provider configuration for the
                tags:
                  - Update
                  - Identity
                  - Providers
                  - Configurations
                  - Domains
                  - Websites
                  - Authorization
                  - Providers
                  - Certificates
                  - Authority
                  - Fleets
                  - Audit
                  - Stream
                  - Configurations
                  - Companies
                  - Networks
                  - Device
                  - Policies
                  - Metadata
                  - Identity
                  - Devices
                  - Domains
                  - Fleets
                  - Resources
                  - ARN
                  - Providers
                  - Authorities
                  - Access
                  - Out
                  - Users
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/worklink-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/worklink-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:worklink
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---