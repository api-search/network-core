---
name: Acknowledge
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/acknowledge.png
url: https://example.com/apis/acknowledge.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Acknowledge
apis:
  - name: iotevents-data
    description: >-
      <p>IoT Events monitors your equipment or device fleets for failures or
      changes in operation, and triggers actions when such events occur. You can
      use IoT Events Data API commands to send inputs to detectors, list
      detectors, and view or update a detector's status.</p> <p> For more
      information, see <a
      href="https://docs.aws.amazon.com/iotevents/latest/developerguide/what-is-iotevents.html">What
      is IoT Events?</a> in the <i>IoT Events Developer Guide</i>.</p>
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
            title: iotevents-data
          paths:
            /alarms/acknowledge:
              POST:
                summary: BatchAcknowledgeAlarm
                description: >-
                  <p>Acknowledges one or more alarms. The alarms change to the
                  <code>ACKNOWLEDGED</code> state after you acknowledge
                  them.</p>
                tags:
                  - Batches
                  - Acknowledge
                  - Alarm
                  - Alarms
                  - Acknowledge
            /detectors/delete:
              POST:
                summary: BatchDeleteDetector
                description: >-
                  <p>Deletes one or more detectors that were created. When a
                  detector is deleted, its state will be cleared and the
                  detector will be removed from the list of detectors. The
                  deleted detector will no longer appear if referenced in the <a
                  href="https://docs.aws.amazon.com/iotevents/latest/apireference/API_iotevents-data_ListDetectors.html">ListDetectors</a>
                  API call.</p>
                tags:
                  - Batches
                  - Delete
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
            /alarms/disable:
              POST:
                summary: BatchDisableAlarm
                description: >-
                  <p>Disables one or more alarms. The alarms change to the
                  <code>DISABLED</code> state after you disable them.</p>
                tags:
                  - Batches
                  - Disable
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
            /alarms/enable:
              POST:
                summary: BatchEnableAlarm
                description: >-
                  <p>Enables one or more alarms. The alarms change to the
                  <code>NORMAL</code> state after you enable them.</p>
                tags:
                  - Batches
                  - Enable
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
            /inputs/messages:
              POST:
                summary: BatchPutMessage
                description: >-
                  <p>Sends a set of messages to the IoT Events system. Each
                  message payload is transformed into the input you specify
                  (<code>"inputName"</code>) and ingested into any detectors
                  that monitor that input. If multiple messages are sent, the
                  order in which the messages are processed isn't guaranteed. To
                  guarantee ordering, you must send messages one at a time and
                  wait for a successful response.</p>
                tags:
                  - Batches
                  - Put
                  - Messages
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
            /alarms/reset:
              POST:
                summary: BatchResetAlarm
                description: >-
                  <p>Resets one or more alarms. The alarms return to the
                  <code>NORMAL</code> state after you reset them.</p>
                tags:
                  - Batches
                  - Reset
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
            /alarms/snooze:
              POST:
                summary: BatchSnoozeAlarm
                description: >-
                  <p>Changes one or more alarms to the snooze mode. The alarms
                  change to the <code>SNOOZE_DISABLED</code> state after you set
                  them to the snooze mode.</p>
                tags:
                  - Batches
                  - Snooze
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
            /detectors:
              POST:
                summary: BatchUpdateDetector
                description: >-
                  <p>Updates the state, variable values, and timer settings of
                  one or more detectors (instances) of a specified detector
                  model.</p>
                tags:
                  - Batches
                  - Update
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
            /alarms/{alarmModelName}/keyValues/:
              GET:
                summary: DescribeAlarm
                description: <p>Retrieves information about an alarm.</p>
                tags:
                  - Describe
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /detectors/{detectorModelName}/keyValues/:
              GET:
                summary: DescribeDetector
                description: >-
                  <p>Returns information about the specified detector
                  (instance).</p>
                tags:
                  - Describe
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /alarms/{alarmModelName}:
              GET:
                summary: ListAlarms
                description: >-
                  <p>Lists one or more alarms. The operation returns only the
                  metadata associated with each alarm.</p>
                tags:
                  - Lists
                  - Alarms
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /detectors/{detectorModelName}:
              GET:
                summary: ListDetectors
                description: <p>Lists detectors (the instances of a detector m
                tags:
                  - Lists
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Value
    overlays:
      - type: APIs.io Search
        url: overlays/iotevents-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotevents-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotevents-data
  - name: privatenetworks
    description: >-
      <p>Amazon Web Services Private 5G is a managed service that makes it easy
      to deploy, operate, and scale your own private mobile network at your
      on-premises location. Private 5G provides the pre-configured hardware and
      software for mobile networks, helps automate setup, and scales capacity on
      demand to support additional devices as needed.</p>
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
            title: privatenetworks
          paths:
            /v1/orders/acknowledge:
              POST:
                summary: AcknowledgeOrderReceipt
                description: >-
                  <p>Acknowledges that the specified network order was
                  received.</p>
                tags:
                  - Acknowledge
                  - Orders
                  - Receipts
                  - V1
                  - Orders
                  - Acknowledge
            /v1/device-identifiers/activate:
              POST:
                summary: ActivateDeviceIdentifier
                description: <p>Activates the specified device identifier.</p>
                tags:
                  - Activate
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
            /v1/network-sites/activate:
              POST:
                summary: ActivateNetworkSite
                description: <p>Activates the specified network site.</p>
                tags:
                  - Activate
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
            /v1/network-resources/configure:
              POST:
                summary: ConfigureAccessPoint
                description: >-
                  <p>Configures the specified network resource. </p> <p> Use
                  this action to specify the geographic position of the
                  hardware. You must provide Certified Professional Installer
                  (CPI) credentials in the request so that we can obtain
                  spectrum grants. For more information, see <a
                  href="https://docs.aws.amazon.com/private-networks/latest/userguide/radio-units.html">Radio
                  units</a> in the <i>Amazon Web Services Private 5G User
                  Guide</i>. </p>
                tags:
                  - Configure
                  - Access
                  - Points
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
            /v1/networks:
              POST:
                summary: CreateNetwork
                description: <p>Creates a network.</p>
                tags:
                  - Create
                  - Networks
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
            /v1/network-sites:
              POST:
                summary: CreateNetworkSite
                description: <p>Creates a network site.</p>
                tags:
                  - Create
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
            /v1/device-identifiers/deactivate:
              POST:
                summary: DeactivateDeviceIdentifier
                description: <p>Deactivates the specified device identifier.</p>
                tags:
                  - Deactivate
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
            /v1/networks/{networkArn}:
              GET:
                summary: GetNetwork
                description: <p>Gets the specified network.</p>
                tags:
                  - Get
                  - Networks
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
            /v1/network-sites/{networkSiteArn}:
              GET:
                summary: GetNetworkSite
                description: <p>Gets the specified network site.</p>
                tags:
                  - Get
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
            /v1/device-identifiers/{deviceIdentifierArn}:
              GET:
                summary: GetDeviceIdentifier
                description: <p>Gets the specified device identifier.</p>
                tags:
                  - Get
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
            /v1/network-resources/{networkResourceArn}:
              GET:
                summary: GetNetworkResource
                description: <p>Gets the specified network resource.</p>
                tags:
                  - Get
                  - Networks
                  - Resources
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
            /v1/orders/{orderArn}:
              GET:
                summary: GetOrder
                description: <p>Gets the specified order.</p>
                tags:
                  - Get
                  - Orders
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
            /v1/device-identifiers/list:
              POST:
                summary: ListDeviceIdentifiers
                description: >-
                  <p>Lists device identifiers. Add filters to your request to
                  return a more specific list of results. Use filters to match
                  the Amazon Resource Name (ARN) of an order, the status of
                  device identifiers, or the ARN of the traffic group.</p> <p>If
                  you specify multiple filters, filters are joined with an OR,
                  and the request returns results that match all of the
                  specified filters.</p>
                tags:
                  - Lists
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/network-resources:
              POST:
                summary: ListNetworkResources
                description: >-
                  <p>Lists network resources. Add filters to your request to
                  return a more specific list of results. Use filters to match
                  the Amazon Resource Name (ARN) of an order or the status of
                  network resources.</p> <p>If you specify multiple filters,
                  filters are joined with an OR, and the request returns results
                  that match all of the specified filters.</p>
                tags:
                  - Lists
                  - Networks
                  - Resources
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/network-sites/list:
              POST:
                summary: ListNetworkSites
                description: >-
                  <p>Lists network sites. Add filters to your request to return
                  a more specific list of results. Use filters to match the
                  status of the network site.</p>
                tags:
                  - Lists
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/networks/list:
              POST:
                summary: ListNetworks
                description: >-
                  <p>Lists networks. Add filters to your request to return a
                  more specific list of results. Use filters to match the status
                  of the network.</p>
                tags:
                  - Lists
                  - Networks
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/orders/list:
              POST:
                summary: ListOrders
                description: >-
                  <p>Lists orders. Add filters to your request to return a more
                  specific list of results. Use filters to match the Amazon
                  Resource Name (ARN) of the network site or the status of the
                  order.</p> <p>If you specify multiple filters, filters are
                  joined with an OR, and the request returns results that match
                  all of the specified filters.</p>
                tags:
                  - Lists
                  - Orders
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /ping:
              GET:
                summary: Ping
                description: <p>Checks the health of the service.</p>
                tags:
                  - Ping
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
            /v1/network-resources/update:
              POST:
                summary: StartNetworkResourceUpdate
                description: >-
                  <p>Use this action to do the following tasks:</p> <ul> <li>
                  <p>Update the duration and renewal status of the commitment
                  period for a radio unit. The update goes into effect
                  immediately.</p> </li> <li> <p>Request a replacement for a
                  network resource.</p> </li> <li> <p>Request that you return a
                  network resource.</p> </li> </ul> <p>After you submit a
                  request to replace or return a network resource, the status of
                  the network resource changes to
                  <code>CREATING_SHIPPING_LABEL</code>. The shipping label is
                  available when the status of the network resource is
                  <code>PENDING_RETURN</code>. After the network resource is
                  successfully returned, its status changes to
                  <code>DELETED</code>. For more information, see <a
                  href="https://docs.aws.amazon.com/private-networks/latest/userguide/radio-units.html#return-radio-unit">Return
                  a radio unit</a>.</p>
                tags:
                  - Start
                  - Networks
                  - Resources
                  - Update
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
                  - Update
            /v1/network-sites/site:
              PUT:
                summary: UpdateNetworkSite
                description: <p>Updates the specified network site.</p>
                tags:
                  - Update
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
                  - Update
            /v1/network-sites/plan:
              PUT:
                summary: UpdateNetworkSitePlan
                description: <p>Updates the specified network site
                tags:
                  - Update
                  - Networks
                  - Sites
                  - Plan
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
                  - Update
                  - Pl
    overlays:
      - type: APIs.io Search
        url: overlays/privatenetworks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/privatenetworks-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:privatenetworks
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---