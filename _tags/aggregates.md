---
name: Aggregates
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/aggregates.png
url: https://example.com/apis/aggregates.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Aggregates
apis:
  - name: iotsitewise
    description: >-
      <p>Welcome to the IoT SiteWise API Reference. IoT SiteWise is an Amazon
      Web Services service that connects <a
      href="https://en.wikipedia.org/wiki/Internet_of_things#Industrial_applications">Industrial
      Internet of Things (IIoT)</a> devices to the power of the Amazon Web
      Services Cloud. For more information, see the <a
      href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/">IoT
      SiteWise User Guide</a>. For information about IoT SiteWise quotas, see <a
      href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/quotas.html">Quotas</a>
      in the <i>IoT SiteWise User Guide</i>.</p>
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
            title: iotsitewise
          paths:
            /assets/{assetId}/associate:
              POST:
                summary: AssociateAssets
                description: >-
                  <p>Associates a child asset with the given parent asset
                  through a hierarchy defined in the parent asset's model. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/add-associated-assets.html">Associating
                  assets</a> in the <i>IoT SiteWise User Guide</i>.</p>
                tags:
                  - Associate
                  - Assets
                  - Identifiers
                  - Associate
            /timeseries/associate/:
              POST:
                summary: AssociateTimeSeriesToAssetProperty
                description: >-
                  <p>Associates a time series (data stream) with an asset
                  property.</p>
                tags:
                  - Associate
                  - Time
                  - Series
                  - To
                  - Assets
                  - Properties
                  - Identifiers
                  - Associate
                  - Time Series
            /projects/{projectId}/assets/associate:
              POST:
                summary: BatchAssociateProjectAssets
                description: >-
                  <p>Associates a group (batch) of assets with an IoT SiteWise
                  Monitor project.</p>
                tags:
                  - Batches
                  - Associate
                  - Projects
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
            /projects/{projectId}/assets/disassociate:
              POST:
                summary: BatchDisassociateProjectAssets
                description: >-
                  <p>Disassociates a group (batch) of assets from an IoT
                  SiteWise Monitor project.</p>
                tags:
                  - Batches
                  - Disassociate
                  - Projects
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
            /properties/batch/aggregates:
              POST:
                summary: BatchGetAssetPropertyAggregates
                description: >-
                  <p>Gets aggregated values (for example, average, minimum, and
                  maximum) for one or more asset properties. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/query-industrial-data.html#aggregates">Querying
                  aggregates</a> in the <i>IoT SiteWise User Guide</i>.</p>
                tags:
                  - Batches
                  - Get
                  - Assets
                  - Properties
                  - Aggregates
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
            /properties/batch/latest:
              POST:
                summary: BatchGetAssetPropertyValue
                description: >-
                  <p>Gets the current value for one or more asset properties.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/query-industrial-data.html#current-values">Querying
                  current values</a> in the <i>IoT SiteWise User Guide</i>.</p>
                tags:
                  - Batches
                  - Get
                  - Assets
                  - Properties
                  - Value
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
            /properties/batch/history:
              POST:
                summary: BatchGetAssetPropertyValueHistory
                description: >-
                  <p>Gets the historical values for one or more asset
                  properties. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/query-industrial-data.html#historical-values">Querying
                  historical values</a> in the <i>IoT SiteWise User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Get
                  - Assets
                  - Properties
                  - Value
                  - History
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
            /properties:
              POST:
                summary: BatchPutAssetPropertyValue
                description: >-
                  <p>Sends a list of asset property values to IoT SiteWise. Each
                  value is a timestamp-quality-value (TQV) data point. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/ingest-api.html">Ingesting
                  data using the API</a> in the <i>IoT SiteWise User
                  Guide</i>.</p> <p>To identify an asset property, you must
                  specify one of the following:</p> <ul> <li> <p>The
                  <code>assetId</code> and <code>propertyId</code> of an asset
                  property.</p> </li> <li> <p>A <code>propertyAlias</code>,
                  which is a data stream alias (for example,
                  <code>/company/windfarm/3/turbine/7/temperature</code>). To
                  define an asset property's alias, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_UpdateAssetProperty.html">UpdateAssetProperty</a>.</p>
                  </li> </ul> <important> <p>With respect to Unix epoch time,
                  IoT SiteWise accepts only TQVs that have a timestamp of no
                  more than 7 days in the past and no more than 10 minutes in
                  the future. IoT SiteWise rejects timestamps outside of the
                  inclusive range of [-7 days, +10 minutes] and returns a
                  <code>TimestampOutOfRangeException</code> error.</p> <p>For
                  each asset property, IoT SiteWise overwrites TQVs with
                  duplicate timestamps unless the newer TQV has a different
                  quality. For example, if you store a TQV <code>{T1, GOOD,
                  V1}</code>, then storing <code>{T1, GOOD, V2}</code> replaces
                  the existing TQV.</p> </important> <p>IoT SiteWise authorizes
                  access to each <code>BatchPutAssetPropertyValue</code> entry
                  individually. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/security_iam_service-with-iam.html#security_iam_service-with-iam-id-based-policies-batchputassetpropertyvalue-action">BatchPutAssetPropertyValue
                  authorization</a> in the <i>IoT SiteWise User Guide</i>.</p>
                tags:
                  - Batches
                  - Put
                  - Assets
                  - Properties
                  - Value
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
            /access-policies:
              GET:
                summary: ListAccessPolicies
                description: >-
                  <p>Retrieves a paginated list of access policies for an
                  identity (an IAM Identity Center user, an IAM Identity Center
                  group, or an IAM user) or an IoT SiteWise Monitor resource (a
                  portal or project).</p>
                tags:
                  - Lists
                  - Access
                  - Policies
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
            /assets:
              GET:
                summary: ListAssets
                description: >-
                  <p>Retrieves a paginated list of asset summaries.</p> <p>You
                  can use this operation to do the following:</p> <ul> <li>
                  <p>List assets based on a specific asset model.</p> </li> <li>
                  <p>List top-level assets.</p> </li> </ul> <p>You can't use
                  this operation to list all assets. To retrieve summaries for
                  all of your assets, use <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_ListAssetModels.html">ListAssetModels</a>
                  to get all of your asset model IDs. Then, use ListAssets to
                  get all assets for each asset model.</p>
                tags:
                  - Lists
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
            /asset-models:
              GET:
                summary: ListAssetModels
                description: >-
                  <p>Retrieves a paginated list of summaries of all asset
                  models.</p>
                tags:
                  - Lists
                  - Assets
                  - Models
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
            /asset-models/{assetModelId}/composite-models:
              GET:
                summary: ListAssetModelCompositeModels
                description: >-
                  <p>Retrieves a paginated list of composite models associated
                  with the asset model</p>
                tags:
                  - Lists
                  - Assets
                  - Models
                  - Composite
                  - Models
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
            /jobs:
              GET:
                summary: ListBulkImportJobs
                description: >-
                  <p>Retrieves a paginated list of bulk import job requests. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/ListBulkImportJobs.html">List
                  bulk import jobs (CLI)</a> in the <i>IoT SiteWise User
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Bulk
                  - Import
                  - Jobs
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
            /dashboards:
              GET:
                summary: ListDashboards
                description: >-
                  <p>Retrieves a paginated list of dashboards for an IoT
                  SiteWise Monitor project.</p>
                tags:
                  - Lists
                  - Dashboards
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
            /20200301/gateways:
              GET:
                summary: ListGateways
                description: <p>Retrieves a paginated list of gateways.</p>
                tags:
                  - Lists
                  - Gateways
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
            /portals:
              GET:
                summary: ListPortals
                description: >-
                  <p>Retrieves a paginated list of IoT SiteWise Monitor
                  portals.</p>
                tags:
                  - Lists
                  - Portals
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
            /projects:
              GET:
                summary: ListProjects
                description: >-
                  <p>Retrieves a paginated list of projects for an IoT SiteWise
                  Monitor portal.</p>
                tags:
                  - Lists
                  - Projects
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
            /access-policies/{accessPolicyId}:
              PUT:
                summary: UpdateAccessPolicy
                description: >-
                  <p>Updates an existing access policy that specifies an
                  identity's access to an IoT SiteWise Monitor portal or project
                  resource.</p>
                tags:
                  - Update
                  - Access
                  - Policies
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /assets/{assetId}:
              PUT:
                summary: UpdateAsset
                description: >-
                  <p>Updates an asset's name. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/update-assets-and-models.html">Updating
                  assets and models</a> in the <i>IoT SiteWise User
                  Guide</i>.</p>
                tags:
                  - Update
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /asset-models/{assetModelId}:
              PUT:
                summary: UpdateAssetModel
                description: >-
                  <p>Updates an asset model and all of the assets that were
                  created from the model. Each asset created from the model
                  inherits the updated asset model's property and hierarchy
                  definitions. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/update-assets-and-models.html">Updating
                  assets and models</a> in the <i>IoT SiteWise User
                  Guide</i>.</p> <important> <p>This operation overwrites the
                  existing model with the provided model. To avoid deleting your
                  asset model's properties or hierarchies, you must include
                  their IDs and definitions in the updated asset model payload.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_DescribeAssetModel.html">DescribeAssetModel</a>.</p>
                  <p>If you remove a property from an asset model, IoT SiteWise
                  deletes all previous data for that property. If you remove a
                  hierarchy definition from an asset model, IoT SiteWise
                  disassociates every asset associated with that hierarchy. You
                  can't change the type or data type of an existing
                  property.</p> </important>
                tags:
                  - Update
                  - Assets
                  - Models
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /asset-models/{assetModelId}/composite-models/{assetModelCompositeModelId}:
              PUT:
                summary: UpdateAssetModelCompositeModel
                description: >-
                  <p>Updates a composite model and all of the assets that were
                  created from the model. Each asset created from the model
                  inherits the updated asset model's property and hierarchy
                  definitions. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/update-assets-and-models.html">Updating
                  assets and models</a> in the <i>IoT SiteWise User
                  Guide</i>.</p> <important> <p>If you remove a property from a
                  composite asset model, IoT SiteWise deletes all previous data
                  for that property. You can’t change the type or data type of
                  an existing property.</p> <p>To replace an existing composite
                  asset model property with a new one with the same
                  <code>name</code>, do the following:</p> <ol> <li> <p>Submit
                  an <code>UpdateAssetModelCompositeModel</code> request with
                  the entire existing property removed.</p> </li> <li> <p>Submit
                  a second <code>UpdateAssetModelCompositeModel</code> request
                  that includes the new property. The new asset property will
                  have the same <code>name</code> as the previous one and IoT
                  SiteWise will generate a new unique <code>id</code>.</p> </li>
                  </ol> </important>
                tags:
                  - Update
                  - Assets
                  - Models
                  - Composite
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /dashboards/{dashboardId}:
              PUT:
                summary: UpdateDashboard
                description: <p>Updates an IoT SiteWise Monitor dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /20200301/gateways/{gatewayId}:
              PUT:
                summary: UpdateGateway
                description: <p>Updates a gateway's name.</p>
                tags:
                  - Update
                  - Gateway
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /portals/{portalId}:
              PUT:
                summary: UpdatePortal
                description: <p>Updates an IoT SiteWise Monitor portal.</p>
                tags:
                  - Update
                  - Portals
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /projects/{projectId}:
              PUT:
                summary: UpdateProject
                description: <p>Updates an IoT SiteWise Monitor project.</p>
                tags:
                  - Update
                  - Projects
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
            /timeseries/delete/:
              POST:
                summary: DeleteTimeSeries
                description: >-
                  <p>Deletes a time series (data stream). If you delete a time
                  series that's associated with an asset property, the asset
                  property still exists, but the time series will no longer be
                  associated with this asset property.</p> <p>To identify a time
                  series, do one of the following:</p> <ul> <li> <p>If the time
                  series isn't associated with an asset property, specify the
                  <code>alias</code> of the time series.</p> </li> <li> <p>If
                  the time series is associated with an asset property, specify
                  one of the following: </p> <ul> <li> <p>The <code>alias</code>
                  of the time series.</p> </li> <li> <p>The <code>assetId</code>
                  and <code>propertyId</code> that identifies the asset
                  property.</p> </li> </ul> </li> </ul>
                tags:
                  - Delete
                  - Time
                  - Series
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
            /actions/{actionId}:
              GET:
                summary: DescribeAction
                description: <p>Retrieves information about an action.</p>
                tags:
                  - Describe
                  - Actions
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
            /assets/{assetId}/composite-models/{assetCompositeModelId}:
              GET:
                summary: DescribeAssetCompositeModel
                description: >-
                  <p>Retrieves information about an asset composite model (also
                  known as an asset component). An
                  <code>AssetCompositeModel</code> is an instance of an
                  <code>AssetModelCompositeModel</code>. If you want to see
                  information about the model this is based on, call <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_DescribeAssetModelCompositeModel.html">DescribeAssetModelCompositeModel</a>.</p>
                tags:
                  - Describe
                  - Assets
                  - Composite
                  - Models
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
            /assets/{assetId}/properties/{propertyId}:
              PUT:
                summary: UpdateAssetProperty
                description: >-
                  <p>Updates an asset property's alias and notification
                  state.</p> <important> <p>This operation overwrites the
                  property's existing alias and notification state. To keep your
                  existing property's alias or notification state, you must
                  include the existing values in the UpdateAssetProperty
                  request. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_DescribeAssetProperty.html">DescribeAssetProperty</a>.</p>
                  </important>
                tags:
                  - Update
                  - Assets
                  - Properties
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
            /jobs/{jobId}:
              GET:
                summary: DescribeBulkImportJob
                description: >-
                  <p>Retrieves information about a bulk import job request. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/DescribeBulkImportJob.html">Describe
                  a bulk import job (CLI)</a> in the <i>Amazon Simple Storage
                  Service User Guide</i>.</p>
                tags:
                  - Describe
                  - Bulk
                  - Import
                  - Jobs
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
            /configuration/account/encryption:
              POST:
                summary: PutDefaultEncryptionConfiguration
                description: >-
                  <p>Sets the default encryption configuration for the Amazon
                  Web Services account. For more information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/key-management.html">Key
                  management</a> in the <i>IoT SiteWise User Guide</i>.</p>
                tags:
                  - Put
                  - Default
                  - Encryption
                  - Configurations
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
            /20200301/gateways/{gatewayId}/capability/{capabilityNamespace}:
              GET:
                summary: DescribeGatewayCapabilityConfiguration
                description: >-
                  <p>Retrieves information about a gateway capability
                  configuration. Each gateway capability defines data sources
                  for a gateway. A capability configuration can contain multiple
                  data source configurations. If you define OPC-UA sources for a
                  gateway in the IoT SiteWise console, all of your OPC-UA
                  sources are stored in one capability configuration. To list
                  all capability configurations for a gateway, use <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_DescribeGateway.html">DescribeGateway</a>.</p>
                tags:
                  - Describe
                  - Gateway
                  - Capabilities
                  - Configurations
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
            /logging:
              PUT:
                summary: PutLoggingOptions
                description: <p>Sets logging options for IoT SiteWise.</p>
                tags:
                  - Put
                  - Logging
                  - Options
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
            /configuration/account/storage:
              POST:
                summary: PutStorageConfiguration
                description: <p>Configures storage settings for IoT SiteWise.</p>
                tags:
                  - Put
                  - Storage
                  - Configurations
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
            /timeseries/describe/:
              GET:
                summary: DescribeTimeSeries
                description: >-
                  <p>Retrieves information about a time series (data
                  stream).</p> <p>To identify a time series, do one of the
                  following:</p> <ul> <li> <p>If the time series isn't
                  associated with an asset property, specify the
                  <code>alias</code> of the time series.</p> </li> <li> <p>If
                  the time series is associated with an asset property, specify
                  one of the following: </p> <ul> <li> <p>The <code>alias</code>
                  of the time series.</p> </li> <li> <p>The <code>assetId</code>
                  and <code>propertyId</code> that identifies the asset
                  property.</p> </li> </ul> </li> </ul>
                tags:
                  - Describe
                  - Time
                  - Series
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
            /assets/{assetId}/disassociate:
              POST:
                summary: DisassociateAssets
                description: >-
                  <p>Disassociates a child asset from the given parent asset
                  through a hierarchy defined in the parent asset's model.</p>
                tags:
                  - Disassociate
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
            /timeseries/disassociate/:
              POST:
                summary: DisassociateTimeSeriesFromAssetProperty
                description: >-
                  <p>Disassociates a time series (data stream) from an asset
                  property.</p>
                tags:
                  - Disassociate
                  - Time
                  - Series
                  - From
                  - Assets
                  - Properties
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
            /actions:
              GET:
                summary: ListActions
                description: >-
                  <p>Retrieves a paginated list of actions for a specific target
                  resource.</p>
                tags:
                  - Lists
                  - Actions
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
            /queries/execution:
              POST:
                summary: ExecuteQuery
                description: >-
                  <p>Run SQL queries to retrieve metadata and time-series data
                  from asset models, assets, measurements, metrics, transforms,
                  and aggregates.</p>
                tags:
                  - Execute
                  - Queries
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
            /properties/aggregates:
              GET:
                summary: GetAssetPropertyAggregates
                description: >-
                  <p>Gets aggregated values for an asset property. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/query-industrial-data.html#aggregates">Querying
                  aggregates</a> in the <i>IoT SiteWise User Guide</i>.</p>
                  <p>To identify an asset property, you must specify one of the
                  following:</p> <ul> <li> <p>The <code>assetId</code> and
                  <code>propertyId</code> of an asset property.</p> </li> <li>
                  <p>A <code>propertyAlias</code>, which is a data stream alias
                  (for example,
                  <code>/company/windfarm/3/turbine/7/temperature</code>). To
                  define an asset property's alias, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_UpdateAssetProperty.html">UpdateAssetProperty</a>.</p>
                  </li> </ul>
                tags:
                  - Get
                  - Assets
                  - Properties
                  - Aggregates
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
            /properties/latest:
              GET:
                summary: GetAssetPropertyValue
                description: >-
                  <p>Gets an asset property's current value. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/query-industrial-data.html#current-values">Querying
                  current values</a> in the <i>IoT SiteWise User Guide</i>.</p>
                  <p>To identify an asset property, you must specify one of the
                  following:</p> <ul> <li> <p>The <code>assetId</code> and
                  <code>propertyId</code> of an asset property.</p> </li> <li>
                  <p>A <code>propertyAlias</code>, which is a data stream alias
                  (for example,
                  <code>/company/windfarm/3/turbine/7/temperature</code>). To
                  define an asset property's alias, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_UpdateAssetProperty.html">UpdateAssetProperty</a>.</p>
                  </li> </ul>
                tags:
                  - Get
                  - Assets
                  - Properties
                  - Value
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
            /properties/history:
              GET:
                summary: GetAssetPropertyValueHistory
                description: >-
                  <p>Gets the history of an asset property's values. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/userguide/query-industrial-data.html#historical-values">Querying
                  historical values</a> in the <i>IoT SiteWise User
                  Guide</i>.</p> <p>To identify an asset property, you must
                  specify one of the following:</p> <ul> <li> <p>The
                  <code>assetId</code> and <code>propertyId</code> of an asset
                  property.</p> </li> <li> <p>A <code>propertyAlias</code>,
                  which is a data stream alias (for example,
                  <code>/company/windfarm/3/turbine/7/temperature</code>). To
                  define an asset property's alias, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_UpdateAssetProperty.html">UpdateAssetProperty</a>.</p>
                  </li> </ul>
                tags:
                  - Get
                  - Assets
                  - Properties
                  - Value
                  - History
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
            /properties/interpolated:
              GET:
                summary: GetInterpolatedAssetPropertyValues
                description: >-
                  <p>Get interpolated values for an asset property for a
                  specified time interval, during a period of time. If your time
                  series is missing data points during the specified time
                  interval, you can use interpolation to estimate the missing
                  data.</p> <p>For example, you can use this operation to return
                  the interpolated temperature values for a wind turbine every
                  24 hours over a duration of 7 days.</p> <p>To identify an
                  asset property, you must specify one of the following:</p>
                  <ul> <li> <p>The <code>assetId</code> and
                  <code>propertyId</code> of an asset property.</p> </li> <li>
                  <p>A <code>propertyAlias</code>, which is a data stream alias
                  (for example,
                  <code>/company/windfarm/3/turbine/7/temperature</code>). To
                  define an asset property's alias, see <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_UpdateAssetProperty.html">UpdateAssetProperty</a>.</p>
                  </li> </ul>
                tags:
                  - Get
                  - Interpolated
                  - Assets
                  - Properties
                  - Values
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
            /asset-models/{assetModelId}/properties:
              GET:
                summary: ListAssetModelProperties
                description: >-
                  <p>Retrieves a paginated list of properties associated with an
                  asset model. If you update properties associated with the
                  model before you finish listing all the properties, you need
                  to start all over again.</p>
                tags:
                  - Lists
                  - Assets
                  - Models
                  - Properties
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
            /assets/{assetId}/properties:
              GET:
                summary: ListAssetProperties
                description: >-
                  <p>Retrieves a paginated list of properties associated with an
                  asset. If you update properties associated with the model
                  before you finish listing all the properties, you need to
                  start all over again.</p>
                tags:
                  - Lists
                  - Assets
                  - Properties
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
            /assets/{assetId}/assetRelationships:
              GET:
                summary: ListAssetRelationships
                description: >-
                  <p>Retrieves a paginated list of asset relationships for an
                  asset. You can use this operation to identify an asset's root
                  asset and all associated assets between that asset and its
                  root.</p>
                tags:
                  - Lists
                  - Assets
                  - Relationships
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
            /assets/{assetId}/hierarchies:
              GET:
                summary: ListAssociatedAssets
                description: >-
                  <p>Retrieves a paginated list of associated assets.</p> <p>You
                  can use this operation to do the following:</p> <ul> <li>
                  <p>List child assets associated to a parent asset by a
                  hierarchy that you specify.</p> </li> <li> <p>List an asset's
                  parent asset.</p> </li> </ul>
                tags:
                  - Lists
                  - Associated
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
                  - Hierarchy
            /asset-models/{assetModelId}/composition-relationships:
              GET:
                summary: ListCompositionRelationships
                description: >-
                  <p>Retrieves a paginated list of composition relationships for
                  an asset model of type <code>COMPONENT_MODEL</code>.</p>
                tags:
                  - Lists
                  - Compositions
                  - Relationships
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
                  - Hierarchy
                  - Compositions
            /projects/{projectId}/assets:
              GET:
                summary: ListProjectAssets
                description: >-
                  <p>Retrieves a paginated list of assets associated with an IoT
                  SiteWise Monitor project.</p>
                tags:
                  - Lists
                  - Projects
                  - Assets
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
                  - Hierarchy
                  - Compositions
            /tags:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from an IoT SiteWise resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
                  - Hierarchy
                  - Compositions
                  - Tags
            /timeseries/:
              GET:
                summary: ListTimeSeries
                description: >-
                  <p>Retrieves a paginated list of time series (data
                  streams).</p>
                tags:
                  - Lists
                  - Time
                  - Series
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
                  - Hierarchy
                  - Compositions
                  - Tags
            /20200301/gateways/{gatewayId}/capability:
              POST:
                summary: UpdateGatewayCapabilityConfiguration
                description: >-
                  <p>Updates a gateway capability configuration or defines a new
                  capability configuration. Each gateway capability defines data
                  sources for a gateway. A capability configuration can contain
                  multiple data source configurations. If you define OPC-UA
                  sources for a gateway in the IoT SiteWise console, all of your
                  OPC-UA sources are stored in one capability configuration. To
                  list all capability configurations for a gateway, use <a
                  href="https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_DescribeGateway.html">DescribeGatewa
                tags:
                  - Update
                  - Gateway
                  - Capabilities
                  - Configurations
                  - Identifiers
                  - Associate
                  - Time Series
                  - Assets
                  - Disassociate
                  - Properties
                  - Batches
                  - Aggregates
                  - Latest
                  - History
                  - Access
                  - Policies
                  - Assets
                  - Models
                  - Models
                  - Composite
                  - Jobs
                  - Dashboards
                  - '20200301'
                  - Gateways
                  - Portals
                  - Projects
                  - Policies
                  - Delete
                  - Properties
                  - Configurations
                  - Account
                  - Encryption
                  - Capabilities
                  - Namespaces
                  - Logging
                  - Storage
                  - Describe
                  - Actions
                  - Queries
                  - Execution
                  - Interpolated
                  - Relationships
                  - Hierarchy
                  - Compositions
                  - Ta
    overlays:
      - type: APIs.io Search
        url: overlays/iotsitewise-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotsitewise-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotsitewise
  - name: FactSet ETF Profile and Prices API
    description: >-
      Access FactSet-collected profile data and pricing for Exchange Traded
      Funds (ETFs).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/etf-profile-and-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#changelog
      - type: OpenAPI
        data:
          host: api.factset.com
          swagger: '2.0'
          consumes:
            - application/json
          produces:
            - application/json
          paths:
            /factset/etf/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Profile
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                description: >-
                  An ETP can be profiled by defining several common attributes
                  such as issuer, fund description, and benchmark.
                summary: Retrieve basic profile information for a specified ETP.
            /factset/etf/allocation/asset/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Asset
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  asset class. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's asset allocations.
            /factset/etf/allocation/country/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Country
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  country names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's country allocations.
            /factset/etf/allocation/currency/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Currency
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  currency. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's currency allocations.
            /factset/etf/allocation/economicDevelopment/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Economic
                  - Development
                  - Status.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  List of allocations classified by a holding's economic
                  development status (e.g. developed market, frontier market,
                  emerging market).
                summary: >-
                  List of allocations classified by a holding's economic
                  development status.
            /factset/etf/allocation/exchange/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Exchange
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  exchanges. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's exchange allocations.
            /factset/etf/allocation/industry/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Industry
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  industry. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's industry allocations.
            /factset/etf/allocation/marketCapitalization/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Total
                  - Market
                  - Capitalization.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  List of allocations classified by a holding's total market
                  capitalization (e.g. Small Cap, Mid Cap, Large Cap). Response
                  will be sorted by weight in descending order.
                summary: >-
                  List of allocations classified by a holding's total market
                  capitalization.
            /factset/etf/allocation/region/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Region
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  region names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's region allocations.
            /factset/etf/allocation/sector/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Sector
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  sector names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's sector allocations.
            /factset/etf/analytics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Analytics
                  - Datapoints
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet's proprietary analytical datapoints include ETP
                  attributes specific to lending, corporate actions, and
                  benchmarks.
                summary: FactSet proprietary analytics datapoints for ETPs.
            /factset/etf/analytics/holdings/statistics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Portfolio
                  - Statistics
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates several proprietary portfolio statistics
                  for ETPs including average maturity, credit quality,
                  price/book ratio, price/earnings ratio, and dividend yield.
                summary: FactSet's portfolio statistics for ETPs.
            /factset/etf/analytics/score/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Rankings.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates various proprietary fund rankings including
                  unique scores, fund grades, segment averages, and
                  recommendations.
                summary: FactSet proprietary ETP rankings.
            /factset/etf/analytics/trade/getBySymbol:
              get:
                tags:
                  - Trade
                  - Statistics
                  - For
                  - Specific
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  Various metrics of an ETP's liquidity including creation
                  metrics, premium/discount, spread, and tracking error
                  statistics.
                summary: Trade statistics for specific ETP.
            /factset/etf/characteristics/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Characteristic
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  An ETP has many unique characteristics specific to its
                  composition that differentiate it from other products. This
                  includes details on leverage, hedging, derivatives, and
                  service providers.
                summary: Retrieve basic characteristic information for a specified ETP.
            /factset/etf/class/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Classification
                  - Specific
                  - To
                  - Asset
                  - Class,
                  - Geography,
                  - Or
                  - Investment
                  - Strategy.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  ETP classification is divided into three categories: Asset
                  Class, Geography, and Investment Strategy. Asset class is
                  determined based on the various asset types held by the fund,
                  A fund's geography can be classified by region (e.g.
                  Asia-Pac), specific geography (e.g. China) or economic
                  development (e.g. BRIC). An ETP's investment strategy is
                  classified in broad categories (e.g. Large Cap) and more
                  granular categorizations.
                summary: >-
                  Retrieve an ETP's classification specific to asset class,
                  geography, or investment strategy.
            /factset/etf/class/category/broad/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Broad
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                description: List of ETP class broad categories.
                summary: List of ETP class broad categories.
            /factset/etf/class/category/focus/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Focus
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                description: List of ETP class focus categories.
                summary: List of ETP class focus categories.
            /factset/etf/class/category/niche/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Niche
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                description: List of ETP class niche categories.
                summary: List of ETP class niche categories.
            /factset/etf/class/geography/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Geographies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: List of ETP class geographies.
                summary: List of ETP class geographies.
            /factset/etf/competitors/listBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Proprietary
                  - List
                  - Of
                  - Competing
                  - Companies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  FactSet defines and maintains a proprietary list of competing
                  companies based on a number of attributes specific to a fund.
                summary: FactSet's proprietary list of competing companies.
            /factset/etf/distribution/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Current
                  - Distribution
                  - Details.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  Retrieve distribution-related details for a specific ETP
                  including dividend and capital gain distribution details.
                summary: Retrieve an ETP's current distribution details.
            /factset/etf/fundFlows/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Cash
                  - Inflow/outflows
                  - For
                  - Various
                  - Time
                  - Periods.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                description: >-
                  Retrieve the amount invested or divested in a specific ETP
                  over various time periods including one-day, one-week,
                  one-month, one-year, and YTD.
                summary: >-
                  Retrieve an ETP's cash inflow/outflows for various time
                  periods.
            /factset/etf/growthOfTenK/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Growth
                  - Of
                  - '10'
                  - Calculated
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Growth of 10K (or growth of 10,000) is a commonly used chart
                  that highlights the change in the value of an initial 10,000
                  investment in the ETP during a given period of time. Often,
                  this period of time is either since inception or the
                  calculation between the pre-defined range.
                summary: >-
                  This endpoint returns selected ETP's Growth of 10K calculated
                  values.
            /factset/etf/holdings/listBySymbol:
              get:
                tags:
                  - Holdings
                  - Details
                  - For
                  - An
                  - Individual
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Retrieve an ETP's holdings information including security,
                  shares held, and weight.
                summary: Holdings details for an individual ETP.
            /factset/etf/marketAggregates/getBySymbol:
              get:
                tags:
                  - Market
                  - Aggregate
                  - Data
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                description: >-
                  Market Aggregates combines FactSet Estimates, FactSet
                  Fundamentals, and FactSet Prices data to derive ratios and per
                  share values on an aggregate level. The resulting index values
                  can be used to identify market trends and compare a
                  combination of portfolios, benchmarks, and individual
                  securities.
                summary: Market aggregate data for ETPs.
            /factset/etf/premiumDiscount/summary/listBySymbol:
              get:
                tags:
                  - Summary
                  - Of
                  - Premium
                  - Discount
                  - Data.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: Summary of ETP premium discount data.
                summary: Summary of ETP premium discount data.
            /factset/etf/price/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  Retrieve an ETP's historical NAV and shares outstanding for a
                  specified time range.
                summary: Retrieve historical ETP NAV values.
            /factset/etf/returns/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Total
                  - Return
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  An ETP's total return data can be returned for various time
                  frames including 1-month, 3-month, YTD, 1-year, 3-year, and
                  5-year. Total return calculations include price performance
                  plus reinvested and compounded distributions. Market price is
                  used to calcualte market returns. Portfolio nav is used to
                  calcualte nav returns.
                summary: Retrieve total return data for a specified ETP.
            /factset/etf/strategy/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Various
                  - Classification
                  - Details
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  ETP's can be classified in many different ways including
                  investment strategy, security weightings, and fund
                  composition.
                summary: Retrieve various classification details for a specified ETP.
            /factset/etf/strategy/segment/list:
              get:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Strategy
                  - Segments.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve the various segments assigned to a specific ETP.
                  Segment data is used to group funds for comparison and
                  relative performance analyses.
                summary: Retrieve a list of ETP strategy segments.
            /factset/etf/structure/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Basic
                  - Structure
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve details on a fund's structure including its type,
                  investment style (active/passive), and legal structure.
                summary: Retrieve the basic structure information for a specified ETP.
            /factset/etf/taxesAndFees/us/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Tax
                  - And
                  - Fee
                  - Related
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                description: >-
                  Retrieve various fee and tax related details on a specified
                  ETP including expense ratio and tax treatment for dividends
                  and capital gains.
                summary: >-
                  Retrieve the tax and fee related information for a specified
                  ETP.
            /factset/etf/timeSeries/listBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                  - Series
                description: >-
                  Retrieve the historical NAV data and the respective fund flows
                  and shares outstanding for a specified fund and time period.
                  Please refer currency.fund in /factset/etf/getBySymbol for
                  currency value.
                summary: Retrieve historical NAV data for a specified ETP.
          info:
            title: Prime Developer Trial
          x-interface-version: 1
          x-documenter-version: 5.38.1
          x-api-version: 2.9.1
          tags:
            - name: factset
              description: factset endpoints
          responses:
            ErrorResponse:
              description: Generic error response for all errors (400 ... 599 error codes)
              schema:
                type: object
                properties:
                  meta:
                    $ref: '#/definitions/ErrorMetaObject'
                  errors:
                    $ref: '#/definitions/ErrorObject'
          definitions:
            ErrorMetaObject:
              type: object
              properties:
                status:
                  $ref: '#/definitions/StatusObject'
            ErrorObject:
              type: array
              description: >-
                The errors member contains additional information about a failed
                request.
              items:
                type: object
                properties:
                  details:
                    type: string
                    description: >-
                      A human-readable, unstructured explanation specific to
                      this occurrence of the failure.
                  encryptedDetails:
                    type: string
                    description: >-
                      Base64-encoded, internal details about the error, in
                      addition to "details".
                  type:
                    type: number
                    format: int32
                    description: Internal error type of the Foundation API protocol.
                  attribute:
                    type: array
                    description: >-
                      For a validation error, a reference to the request
                      parameter that failed validation; otherwise, an empty
                      array.
                    items:
                      type: object
                      properties:
                        name:
                          type: string
                          description: Element of the path denoting the request parameter.
                        index:
                          type: number
                          format: int32
                          description: >-
                            If the attribute "name" designates an array, index
                            of the array element; otherwise the special value
                            -1.
                      x-property-sort:
                        - name
                        - index
                x-property-sort:
                  - detail
                  - encryptedDetails
                  - type
                  - attribute
            AttributesMember:
              type: array
              description: >-
                Limit the attributes returned in the response to the specified
                set.
              items:
                type: string
                maxLength: 100
                exclusiveMaximum: false
              maxItems: 50
              uniqueItems: true
            LanguageMember:
              type: string
              format: isoLanguage
              description: ISO 639-1 code of the language.
              maxLength: 2
              minLength: 2
              exclusiveMinimum: false
              exclusiveMaximum: false
            StatusObject:
              type: object
              properties:
                code:
                  type: number
                  format: int32
                  description: >-
                    The HTTP status code of the response, mirroring the code
                    from the Status-Line of the HTTP response message (see
                    [RFC2616] section 6.1).
              description: The status member contains the status code of the response.
              required:
                - code
            CursorBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the cursor-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of `total` is estimated.
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - total
                - isEstimatedTotal
                - next
                - previous
              x-property-sort:
                - total
                - isEstimatedTotal
                - next
                - previous
            CursorBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the cursor-based pagination strategy;
                a total element count is not supported.
              properties:
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - next
                - previous
              x-property-sort:
                - next
                - previous
            OffsetBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the offset-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of "total" is estimated.
              required:
                - total
                - isEstimatedTotal
              x-property-sort:
                - total
                - isEstimatedTotal
            OffsetBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the offset-based pagination strategy;
                a total element count is not supported.
              properties:
                hasNext:
                  type: boolean
                  description: >-
                    Flag indicating that a subsequent request with the same
                    parameters, except that the parameter `pagination.offset` is
                    incremented by `pagination.limit`, would yield additional
                    results.
              required:
                - hasNext
              x-property-sort:
                - hasNext
            PartialOutputObject:
              type: object
              properties:
                isPartial:
                  type: boolean
                  description: >-
                    Flag indicating that the response is a possibly incomplete
                    array or an object containing a possibly incomplete array,
                    due to hitting a processing time limit. If `true`, some
                    matching results might be missing from the array, or
                    elements for matching results might be incorrectly included
                    (for example, when priority sorting would have removed the
                    element). Depending on the use case, such a response may be
                    unsuitable.
              description: >-
                Object denoting that the endpoint response is possibly
                incomplete.
              required:
                - isPartial
              x-property-sort:
                - isPartial
          basePath: /wealth/v1
          schemes:
            - https
          securityDefinitions:
            Basic:
              type: nu
    overlays:
      - type: APIs.io Search
        url: overlays/etf-profile-and-prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/etf-profile-and-prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-etf-profile-and-prices-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---