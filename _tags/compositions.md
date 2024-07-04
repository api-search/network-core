---
name: Compositions
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/compositions.png
url: https://example.com/apis/compositions.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Compositions
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
  - name: ivs-realtime
    description: >-
      <p> <b>Introduction</b> </p> <p>The Amazon Interactive Video Service (IVS)
      real-time API is REST compatible, using a standard HTTP API and an AWS
      EventBridge event stream for responses. JSON is used for both requests and
      responses, including errors. </p> <p>Terminology:</p> <ul> <li> <p>A
      <i>stage</i> is a virtual space where participants can exchange video in
      real time.</p> </li> <li> <p>A <i>participant token</i> is a token that
      authenticates a participant when they join a stage.</p> </li> <li> <p>A
      <i>participant object</i> represents participants (people) in the stage
      and contains information about them. When a token is created, it includes
      a participant ID; when a participant uses that token to join a stage, the
      participant is associated with that participant ID. There is a 1:1 mapping
      between participant tokens and participants.</p> </li> <li> <p>Server-side
      composition: The <i>composition</i> process composites participants of a
      stage into a single video and forwards it to a set of outputs (e.g., IVS
      channels). Composition endpoints support this process.</p> </li> <li>
      <p>Server-side composition: A <i>composition</i> controls the look of the
      outputs, including how participants are positioned in the video.</p> </li>
      </ul> <p> <b>Resources</b> </p> <p>The following resources contain
      information about your IVS live stream (see <a
      href="https://docs.aws.amazon.com/ivs/latest/RealTimeUserGuide/getting-started.html">Getting
      Started with Amazon IVS Real-Time Streaming</a>):</p> <ul> <li> <p>
      <b>Stage</b> — A stage is a virtual space where participants can exchange
      video in real time.</p> </li> </ul> <p> <b>Tagging</b> </p> <p>A
      <i>tag</i> is a metadata label that you assign to an AWS resource. A tag
      comprises a <i>key</i> and a <i>value</i>, both set by you. For example,
      you might set a tag as <code>topic:nature</code> to label a particular
      video category. See <a
      href="https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html">Tagging
      AWS Resources</a> for more information, including restrictions that apply
      to tags and "Tag naming limits and requirements"; Amazon IVS stages has no
      service-specific constraints beyond what is documented there.</p> <p>Tags
      can help you identify and organize your AWS resources. For example, you
      can use the same tag for different resources to indicate that they are
      related. You can also use tags to manage access (see <a
      href="https://docs.aws.amazon.com/IAM/latest/UserGuide/access_tags.html">Access
      Tags</a>).</p> <p>The Amazon IVS real-time API has these tag-related
      endpoints: <a>TagResource</a>, <a>UntagResource</a>, and
      <a>ListTagsForResource</a>. The following resource supports tagging:
      Stage.</p> <p>At most 50 tags can be applied to a resource.</p> <p>
      <b>Stages Endpoints</b> </p> <ul> <li> <p> <a>CreateParticipantToken</a> —
      Creates an additional token for a specified stage. This can be done after
      stage creation or when tokens expire.</p> </li> <li> <p>
      <a>CreateStage</a> — Creates a new stage (and optionally participant
      tokens).</p> </li> <li> <p> <a>DeleteStage</a> — Shuts down and deletes
      the specified stage (disconnecting all participants).</p> </li> <li> <p>
      <a>DisconnectParticipant</a> — Disconnects a specified participant and
      revokes the participant permanently from a specified stage.</p> </li> <li>
      <p> <a>GetParticipant</a> — Gets information about the specified
      participant token.</p> </li> <li> <p> <a>GetStage</a> — Gets information
      for the specified stage.</p> </li> <li> <p> <a>GetStageSession</a> — Gets
      information for the specified stage session.</p> </li> <li> <p>
      <a>ListParticipantEvents</a> — Lists events for a specified participant
      that occurred during a specified stage session.</p> </li> <li> <p>
      <a>ListParticipants</a> — Lists all participants in a specified stage
      session.</p> </li> <li> <p> <a>ListStages</a> — Gets summary information
      about all stages in your account, in the AWS region where the API request
      is processed.</p> </li> <li> <p> <a>ListStageSessions</a> — Gets all
      sessions for a specified stage.</p> </li> <li> <p> <a>UpdateStage</a> —
      Updates a stage’s configuration.</p> </li> </ul> <p> <b>Composition
      Endpoints</b> </p> <ul> <li> <p> <a>GetComposition</a> — Gets information
      about the specified Composition resource.</p> </li> <li> <p>
      <a>ListCompositions</a> — Gets summary information about all Compositions
      in your account, in the AWS region where the API request is processed.</p>
      </li> <li> <p> <a>StartComposition</a> — Starts a Composition from a stage
      based on the configuration provided in the request.</p> </li> <li> <p>
      <a>StopComposition</a> — Stops and deletes a Composition resource. Any
      broadcast from the Composition resource is stopped.</p> </li> </ul> <p>
      <b>EncoderConfiguration Endpoints</b> </p> <ul> <li> <p>
      <a>CreateEncoderConfiguration</a> — Creates an EncoderConfiguration
      object.</p> </li> <li> <p> <a>DeleteEncoderConfiguration</a> — Deletes an
      EncoderConfiguration resource. Ensures that no Compositions are using this
      template; otherwise, returns an error.</p> </li> <li> <p>
      <a>GetEncoderConfiguration</a> — Gets information about the specified
      EncoderConfiguration resource.</p> </li> <li> <p>
      <a>ListEncoderConfigurations</a> — Gets summary information about all
      EncoderConfigurations in your account, in the AWS region where the API
      request is processed.</p> </li> </ul> <p> <b>StorageConfiguration
      Endpoints</b> </p> <ul> <li> <p> <a>CreateStorageConfiguration</a> —
      Creates a new storage configuration, used to enable recording to Amazon
      S3.</p> </li> <li> <p> <a>DeleteStorageConfiguration</a> — Deletes the
      storage configuration for the specified ARN.</p> </li> <li> <p>
      <a>GetStorageConfiguration</a> — Gets the storage configuration for the
      specified ARN.</p> </li> <li> <p> <a>ListStorageConfigurations</a> — Gets
      summary information about all storage configurations in your account, in
      the AWS region where the API request is processed.</p> </li> </ul> <p>
      <b>Tags Endpoints</b> </p> <ul> <li> <p> <a>ListTagsForResource</a> — Gets
      information about AWS tags for the specified ARN.</p> </li> <li> <p>
      <a>TagResource</a> — Adds or updates tags for the AWS resource with the
      specified ARN.</p> </li> <li> <p> <a>UntagResource</a> — Removes tags from
      the resource with the specified ARN.</p> </li> </ul>
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
            title: ivs-realtime
          paths:
            /CreateEncoderConfiguration:
              POST:
                summary: CreateEncoderConfiguration
                description: <p>Creates an EncoderConfiguration object.</p>
                tags:
                  - Create
                  - Encoder
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
            /CreateParticipantToken:
              POST:
                summary: CreateParticipantToken
                description: >-
                  <p>Creates an additional token for a specified stage. This can
                  be done after stage creation or when tokens expire. Tokens
                  always are scoped to the stage for which they are created.</p>
                  <p>Encryption keys are owned by Amazon IVS and never used
                  directly by your application.</p>
                tags:
                  - Create
                  - Participants
                  - Tokens
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
            /CreateStage:
              POST:
                summary: CreateStage
                description: >-
                  <p>Creates a new stage (and optionally participant
                  tokens).</p>
                tags:
                  - Create
                  - Stage
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
            /CreateStorageConfiguration:
              POST:
                summary: CreateStorageConfiguration
                description: >-
                  <p>Creates a new storage configuration, used to enable
                  recording to Amazon S3. When a StorageConfiguration is
                  created, IVS will modify the S3 bucketPolicy of the provided
                  bucket. This will ensure that IVS has sufficient permissions
                  to write content to the provided bucket.</p>
                tags:
                  - Create
                  - Storage
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
            /DeleteEncoderConfiguration:
              POST:
                summary: DeleteEncoderConfiguration
                description: >-
                  <p>Deletes an EncoderConfiguration resource. Ensures that no
                  Compositions are using this template; otherwise, returns an
                  error.</p>
                tags:
                  - Delete
                  - Encoder
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
            /DeleteStage:
              POST:
                summary: DeleteStage
                description: >-
                  <p>Shuts down and deletes the specified stage (disconnecting
                  all participants).</p>
                tags:
                  - Delete
                  - Stage
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
            /DeleteStorageConfiguration:
              POST:
                summary: DeleteStorageConfiguration
                description: >-
                  <p>Deletes the storage configuration for the specified
                  ARN.</p> <p>If you try to delete a storage configuration that
                  is used by a Composition, you will get an error (409
                  ConflictException). To avoid this, for all Compositions that
                  reference the storage configuration, first use
                  <a>StopComposition</a> and wait for it to complete, then use
                  DeleteStorageConfiguration.</p>
                tags:
                  - Delete
                  - Storage
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
            /DisconnectParticipant:
              POST:
                summary: DisconnectParticipant
                description: >-
                  <p>Disconnects a specified participant and revokes the
                  participant permanently from a specified stage.</p>
                tags:
                  - Disconnect
                  - Participants
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
            /GetComposition:
              POST:
                summary: GetComposition
                description: >-
                  <p>Get information about the specified Composition
                  resource.</p>
                tags:
                  - Get
                  - Compositions
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
            /GetEncoderConfiguration:
              POST:
                summary: GetEncoderConfiguration
                description: >-
                  <p>Gets information about the specified EncoderConfiguration
                  resource. </p>
                tags:
                  - Get
                  - Encoder
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
            /GetParticipant:
              POST:
                summary: GetParticipant
                description: <p>Gets information about the specified participant token.</p>
                tags:
                  - Get
                  - Participants
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
            /GetStage:
              POST:
                summary: GetStage
                description: <p>Gets information for the specified stage.</p>
                tags:
                  - Get
                  - Stage
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
            /GetStageSession:
              POST:
                summary: GetStageSession
                description: <p>Gets information for the specified stage session.</p>
                tags:
                  - Get
                  - Stage
                  - Sessions
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
            /GetStorageConfiguration:
              POST:
                summary: GetStorageConfiguration
                description: <p>Gets the storage configuration for the specified ARN.</p>
                tags:
                  - Get
                  - Storage
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
            /ListCompositions:
              POST:
                summary: ListCompositions
                description: >-
                  <p>Gets summary information about all Compositions in your
                  account, in the AWS region where the API request is processed.
                  </p>
                tags:
                  - Lists
                  - Compositions
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
            /ListEncoderConfigurations:
              POST:
                summary: ListEncoderConfigurations
                description: >-
                  <p>Gets summary information about all EncoderConfigurations in
                  your account, in the AWS region where the API request is
                  processed.</p>
                tags:
                  - Lists
                  - Encoder
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
            /ListParticipantEvents:
              POST:
                summary: ListParticipantEvents
                description: >-
                  <p>Lists events for a specified participant that occurred
                  during a specified stage session.</p>
                tags:
                  - Lists
                  - Participants
                  - Events
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
            /ListParticipants:
              POST:
                summary: ListParticipants
                description: <p>Lists all participants in a specified stage session.</p>
                tags:
                  - Lists
                  - Participants
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
            /ListStageSessions:
              POST:
                summary: ListStageSessions
                description: <p>Gets all sessions for a specified stage.</p>
                tags:
                  - Lists
                  - Stage
                  - Sessions
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
            /ListStages:
              POST:
                summary: ListStages
                description: >-
                  <p>Gets summary information about all stages in your account,
                  in the AWS region where the API request is processed.</p>
                tags:
                  - Lists
                  - Stages
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
                  - Stages
            /ListStorageConfigurations:
              POST:
                summary: ListStorageConfigurations
                description: >-
                  <p>Gets summary information about all storage configurations
                  in your account, in the AWS region where the API request is
                  processed.</p>
                tags:
                  - Lists
                  - Storage
                  - Configurations
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
                  - Stages
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from the resource with the specified ARN.</p>
                tags:
                  - Untag
                  - Resources
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
                  - Stages
                  - ARN
            /StartComposition:
              POST:
                summary: StartComposition
                description: >-
                  <p>Starts a Composition from a stage based on the
                  configuration provided in the request.</p> <p>A Composition is
                  an ephemeral resource that exists after this endpoint returns
                  successfully. Composition stops and the resource is
                  deleted:</p> <ul> <li> <p>When <a>StopComposition</a> is
                  called.</p> </li> <li> <p>After a 1-minute timeout, when all
                  participants are disconnected from the stage.</p> </li> <li>
                  <p>After a 1-minute timeout, if there are no participants in
                  the stage when StartComposition is called.</p> </li> <li>
                  <p>When broadcasting to the IVS channel fails and all retries
                  are exhausted.</p> </li> <li> <p>When broadcasting is
                  disconnected and all attempts to reconnect are exhausted.</p>
                  </li> </ul>
                tags:
                  - Start
                  - Compositions
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
                  - Stages
                  - ARN
                  - Start
            /StopComposition:
              POST:
                summary: StopComposition
                description: >-
                  <p>Stops and deletes a Composition resource. Any broadcast
                  from the Composition resource is stopped.</p>
                tags:
                  - Stop
                  - Compositions
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
                  - Stages
                  - ARN
                  - Start
                  - Stop
            /UpdateStage:
              POST:
                summary: UpdateStage
                description: <p>Updates a stage’s configur
                tags:
                  - Update
                  - Stage
                  - Create
                  - Encoder
                  - Configurations
                  - Participants
                  - Tokens
                  - Stage
                  - Storage
                  - Delete
                  - Disconnect
                  - Get
                  - Compositions
                  - Sessions
                  - Lists
                  - Compositions
                  - Configurations
                  - Events
                  - Participants
                  - Sessions
                  - Stages
                  - ARN
                  - Start
                  - Stop
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/ivs-realtime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ivs-realtime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ivs-realtime
  - aid: twilio:twilio-video-api
    name: Twilio Video API
    description: >-
      Twilio Video is a programmable real-time communications platform that
      allows you to add video chat functionality to your web, iOS, and Android
      applications. The platform provides APIs, SDKs, and helper tools to
      capture, distribute, record, and render high quality audio and video
      applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/docs/video
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/docs/video
      - type: OpenAPI
        data:
          info:
            title: Twilio - Video
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Compositions/{Sid}:
              description: Recording compositions
              get:
                description: >-
                  Returns a single Composition resource identified by a
                  Composition SID.
                tags:
                  - Compositions
                  - Sid
              delete:
                description: >-
                  Delete a Recording Composition resource identified by a
                  Composition SID.
                tags:
                  - Compositions
                  - Sid
            /v1/Compositions:
              description: Recording compositions
              get:
                description: List of all Recording compositions.
                tags:
                  - Compositions
                  - Sid
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
            /v1/CompositionHooks/{Sid}:
              description: Recording composition hooks
              get:
                description: >-
                  Returns a single CompositionHook resource identified by a
                  CompositionHook SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
              delete:
                description: >-
                  Delete a Recording CompositionHook resource identified by a
                  `CompositionHook SID`.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
            /v1/CompositionHooks:
              description: Recording composition hooks
              get:
                description: List of all Recording CompositionHook resources.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
            /v1/CompositionSettings/Default:
              description: Recording composition settings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
            /v1/Recordings/{Sid}:
              description: Single-track, single-media recordings
              get:
                description: >-
                  Returns a single Recording resource identified by a Recording
                  SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
              delete:
                description: Delete a Recording resource identified by a Recording SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
            /v1/Recordings:
              description: Single-track, single-media recordings
              get:
                description: List of all Track recordings.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
            /v1/RecordingSettings/Default:
              description: Recording settings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
            /v1/Rooms/{Sid}:
              description: Video rooms with one or more participants
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
            /v1/Rooms:
              description: Video rooms with one or more participants
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
            /v1/Rooms/{RoomSid}/Participants/{Sid}:
              description: Participants in video rooms
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
            /v1/Rooms/{RoomSid}/Participants:
              description: Participants in video rooms
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
            /v1/Rooms/{RoomSid}/Participants/{Sid}/Anonymize:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/PublishedTracks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a single Track resource represented by TrackName or
                  SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/PublishedTracks:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a list of tracks associated with a given Participant.
                  Only `currently` Published Tracks are in the list resource.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/SubscribeRules:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns a list of Subscribe Rules for the Participant.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
              post:
                description: Update the Subscribe Rules for the Participant
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/SubscribedTracks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a single Track resource represented by `track_sid`. 
                  Note: This is one resource with the Video API that requires a
                  SID, be Track Name on the subscriber side is not guaranteed to
                  be unique.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/SubscribedTracks:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a list of tracks that are subscribed for the
                  participant.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/Recordings/{Sid}:
              description: Single-track, single-media room recordings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
              delete:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/Recordings:
              description: Single-track, single-media room recordings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/RecordingRules:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns a list of Recording Rules for the Room.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
              post:
                description: Update the Recording Rules for the Room
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
          tags:
            - name: VideoV1Anonymize
            - name: VideoV1Composition
            - name: VideoV1CompositionHook
            - name: VideoV1CompositionSettings
            - name: VideoV1Participant
            - name: VideoV1PublishedTrack
            - name: VideoV1Recording
            - name: VideoV1RecordingRules
            - name: VideoV1RecordingSettings
            - name: VideoV1Room
            - name: VideoV1RoomRecording
            - name: VideoV1SubscribeRules
            - name: VideoV1SubscribedTrack
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/video-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/video-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---