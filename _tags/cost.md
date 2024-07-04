---
name: Cost
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cost.png
url: https://example.com/apis/cost.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cost
apis:
  - name: Adyen BinLookup API
    description: >-
      The BIN Lookup API provides endpoints for retrieving information, such as
      cost estimates, and 3D Secure supported version based on a given BIN.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/BinLookup/52/overview
    baseURL: https://pal-test.adyen.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/BinLookup/52/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen BinLookup API
          tags:
            - name: General
          paths:
            /get3dsAvailability:
              post:
                tags:
                  - Checks
                  - If
                  - Secure
                  - Is
                  - Available
                  - Availability
                summary: Check if 3D Secure is available
                description: >-
                  Verifies whether 3D Secure is available for the specified BIN
                  or card brand. For 3D Secure 2, this endpoint also returns
                  device fingerprinting keys.


                  For more information, refer to [3D Secure
                  2](https://docs.adyen.com/online-payments/3d-secure/native-3ds2).
            /getCostEstimate:
              post:
                tags:
                  - Get
                  - Fees
                  - Cost
                  - Estimates
                  - Availability
                  - Cost
                  - Estimates
                summary: Get a fees cost estimate
                description: >-
                  >This API is available only for merchants operating in
                  Australia, the EU, and the UK.


                  Use the Adyen Cost Estimation API to pre-calculate interchange
                  and scheme fee costs. Knowing these costs prior actual payment
                  authorisation gives you an opportunity to charge those costs
                  to the cardholder, if necessary.


                  To retrieve this information, make the call to the
                  `/getCostEstimate` endpoint. The response to this call
                  contains the amount of the interchange and scheme fees charged
                  by the network for this transaction, and also which
                  surcharging policy is possible (based on current regulations).


                  > Since not all information is known in advance (for example,
                  if the cardholder will successfully authenticate via 3D Secure
                  or if you also plan to provide additional Level 2/3 data), the
                  returned amounts are based on a set of assumption criteria you
                  defi
    overlays:
      - type: APIs.io Search
        url: overlays/binlookup-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/binlookup-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-binlookup-api
  - name: billingconductor
    description: >-
      <p>Amazon Web Services Billing Conductor is a fully managed service that
      you can use to customize a <a
      href="https://docs.aws.amazon.com/billingconductor/latest/userguide/understanding-eb.html#eb-other-definitions">proforma</a>
      version of your billing data each month, to accurately show or chargeback
      your end customers. Amazon Web Services Billing Conductor doesn't change
      the way you're billed by Amazon Web Services each month by design.
      Instead, it provides you with a mechanism to configure, generate, and
      display rates to certain customers over a given billing period. You can
      also analyze the difference between the rates you apply to your accounting
      groupings relative to your actual rates from Amazon Web Services. As a
      result of your Amazon Web Services Billing Conductor configuration, the
      payer account can also see the custom rate applied on the billing details
      page of the <a href="https://console.aws.amazon.com/billing">Amazon Web
      Services Billing console</a>, or configure a cost and usage report per
      billing group.</p> <p>This documentation shows how you can configure
      Amazon Web Services Billing Conductor using its API. For more information
      about using the <a
      href="https://console.aws.amazon.com/billingconductor/">Amazon Web
      Services Billing Conductor</a> user interface, see the <a
      href="https://docs.aws.amazon.com/billingconductor/latest/userguide/what-is-billingconductor.html">
      Amazon Web Services Billing Conductor User Guide</a>.</p>
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
            title: billingconductor
          paths:
            /associate-accounts:
              POST:
                summary: AssociateAccounts
                description: >-
                  <p>Connects an array of account IDs in a consolidated billing
                  family to a predefined billing group. The account IDs must be
                  a part of the consolidated billing family during the current
                  month, and not already associated with another billing group.
                  The maximum number of accounts that can be associated in one
                  call is 30. </p>
                tags:
                  - Associate
                  - Accounts
                  - Associate
                  - Accounts
            /associate-pricing-rules:
              PUT:
                summary: AssociatePricingRules
                description: >-
                  <p>Connects an array of <code>PricingRuleArns</code> to a
                  defined <code>PricingPlan</code>. The maximum number
                  <code>PricingRuleArn</code> that can be associated in one call
                  is 30. </p>
                tags:
                  - Associate
                  - Pricing
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
            /batch-associate-resources-to-custom-line-item:
              PUT:
                summary: BatchAssociateResourcesToCustomLineItem
                description: >-
                  <p> Associates a batch of resources to a percentage custom
                  line item. </p>
                tags:
                  - Batches
                  - Associate
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
            /batch-disassociate-resources-from-custom-line-item:
              PUT:
                summary: BatchDisassociateResourcesFromCustomLineItem
                description: >-
                  <p> Disassociates a batch of resources from a percentage
                  custom line item. </p>
                tags:
                  - Batches
                  - Disassociate
                  - Resources
                  - From
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
            /create-billing-group:
              POST:
                summary: CreateBillingGroup
                description: >-
                  <p> Creates a billing group that resembles a consolidated
                  billing family that Amazon Web Services charges, based off of
                  the predefined pricing plan computation. </p>
                tags:
                  - Create
                  - Billing
                  - Group
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
            /create-custom-line-item:
              POST:
                summary: CreateCustomLineItem
                description: >-
                  <p>Creates a custom line item that can be used to create a
                  one-time fixed charge that can be applied to a single billing
                  group for the current or previous billing period. The one-time
                  fixed charge is either a fee or discount. </p>
                tags:
                  - Create
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
            /create-pricing-plan:
              POST:
                summary: CreatePricingPlan
                description: >-
                  <p>Creates a pricing plan that is used for computing Amazon
                  Web Services charges for billing groups. </p>
                tags:
                  - Create
                  - Pricing
                  - Plan
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
            /create-pricing-rule:
              POST:
                summary: CreatePricingRule
                description: >-
                  <p> Creates a pricing rule can be associated to a pricing
                  plan, or a set of pricing plans. </p>
                tags:
                  - Create
                  - Pricing
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
            /delete-billing-group:
              POST:
                summary: DeleteBillingGroup
                description: <p> Deletes a billing group. </p>
                tags:
                  - Delete
                  - Billing
                  - Group
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
            /delete-custom-line-item:
              POST:
                summary: DeleteCustomLineItem
                description: >-
                  <p> Deletes the custom line item identified by the given ARN
                  in the current, or previous billing period. </p>
                tags:
                  - Delete
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
            /delete-pricing-plan:
              POST:
                summary: DeletePricingPlan
                description: >-
                  <p>Deletes a pricing plan. The pricing plan must not be
                  associated with any billing groups to delete successfully.</p>
                tags:
                  - Delete
                  - Pricing
                  - Plan
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
            /delete-pricing-rule:
              POST:
                summary: DeletePricingRule
                description: >-
                  <p> Deletes the pricing rule that's identified by the input
                  Amazon Resource Name (ARN). </p>
                tags:
                  - Delete
                  - Pricing
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
            /disassociate-accounts:
              POST:
                summary: DisassociateAccounts
                description: >-
                  <p>Removes the specified list of account IDs from the given
                  billing group. </p>
                tags:
                  - Disassociate
                  - Accounts
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
            /disassociate-pricing-rules:
              PUT:
                summary: DisassociatePricingRules
                description: >-
                  <p> Disassociates a list of pricing rules from a pricing plan.
                  </p>
                tags:
                  - Disassociate
                  - Pricing
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
            /get-billing-group-cost-report:
              POST:
                summary: GetBillingGroupCostReport
                description: >-
                  <p>Retrieves the margin summary report, which includes the
                  Amazon Web Services cost and charged amount (pro forma cost)
                  by Amazon Web Service for a specific billing group.</p>
                tags:
                  - Get
                  - Billing
                  - Group
                  - Cost
                  - Reports
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
            /list-account-associations:
              POST:
                summary: ListAccountAssociations
                description: >-
                  <p> This is a paginated call to list linked accounts that are
                  linked to the payer account for the specified time period. If
                  no information is provided, the current billing period is
                  used. The response will optionally include the billing group
                  that's associated with the linked account.</p>
                tags:
                  - Lists
                  - Account
                  - Associations
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
            /list-billing-group-cost-reports:
              POST:
                summary: ListBillingGroupCostReports
                description: >-
                  <p>A paginated call to retrieve a summary report of actual
                  Amazon Web Services charges and the calculated Amazon Web
                  Services charges based on the associated pricing plan of a
                  billing group.</p>
                tags:
                  - Lists
                  - Billing
                  - Group
                  - Cost
                  - Reports
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
            /list-billing-groups:
              POST:
                summary: ListBillingGroups
                description: >-
                  <p>A paginated call to retrieve a list of billing groups for
                  the given billing period. If you don't provide a billing
                  group, the current billing period is used.</p>
                tags:
                  - Lists
                  - Billing
                  - Groups
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
            /list-custom-line-item-versions:
              POST:
                summary: ListCustomLineItemVersions
                description: >-
                  <p>A paginated call to get a list of all custom line item
                  versions.</p>
                tags:
                  - Lists
                  - Custom
                  - Line
                  - Items
                  - Versions
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
            /list-custom-line-items:
              POST:
                summary: ListCustomLineItems
                description: >-
                  <p> A paginated call to get a list of all custom line items
                  (FFLIs) for the given billing period. If you don't provide a
                  billing period, the current billing period is used. </p>
                tags:
                  - Lists
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
            /list-pricing-plans:
              POST:
                summary: ListPricingPlans
                description: >-
                  <p>A paginated call to get pricing plans for the given billing
                  period. If you don't provide a billing period, the current
                  billing period is used. </p>
                tags:
                  - Lists
                  - Pricing
                  - Plans
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
            /list-pricing-plans-associated-with-pricing-rule:
              POST:
                summary: ListPricingPlansAssociatedWithPricingRule
                description: >-
                  <p> A list of the pricing plans that are associated with a
                  pricing rule. </p>
                tags:
                  - Lists
                  - Pricing
                  - Plans
                  - Associated
                  - null
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
            /list-pricing-rules:
              POST:
                summary: ListPricingRules
                description: >-
                  <p> Describes a pricing rule that can be associated to a
                  pricing plan, or set of pricing plans. </p>
                tags:
                  - Lists
                  - Pricing
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
            /list-pricing-rules-associated-to-pricing-plan:
              POST:
                summary: ListPricingRulesAssociatedToPricingPlan
                description: >-
                  <p> Lists the pricing rules that are associated with a pricing
                  plan. </p>
                tags:
                  - Lists
                  - Pricing
                  - Rules
                  - Associated
                  - To
                  - Plan
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
            /list-resources-associated-to-custom-line-item:
              POST:
                summary: ListResourcesAssociatedToCustomLineItem
                description: >-
                  <p> List the resources that are associated to a custom line
                  item. </p>
                tags:
                  - Lists
                  - Resources
                  - Associated
                  - To
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p> Deletes specified tags from a resource. </p>
                tags:
                  - Untag
                  - Resources
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
                  - Resources
                  - ARN
            /update-billing-group:
              POST:
                summary: UpdateBillingGroup
                description: <p>This updates an existing billing group. </p>
                tags:
                  - Update
                  - Billing
                  - Group
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
                  - Resources
                  - ARN
                  - Update
            /update-custom-line-item:
              POST:
                summary: UpdateCustomLineItem
                description: >-
                  <p> Update an existing custom line item in the current or
                  previous billing period. </p>
                tags:
                  - Update
                  - Custom
                  - Line
                  - Items
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
                  - Resources
                  - ARN
                  - Update
            /update-pricing-plan:
              PUT:
                summary: UpdatePricingPlan
                description: <p>This updates an existing pricing plan. </p>
                tags:
                  - Update
                  - Pricing
                  - Plan
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
                  - Resources
                  - ARN
                  - Update
            /update-pricing-rule:
              PUT:
                summary: UpdatePricingRule
                description: <p> Updates an existing pricing
                tags:
                  - Update
                  - Pricing
                  - Rules
                  - Associate
                  - Accounts
                  - Pricing
                  - Rules
                  - Batches
                  - Resources
                  - To
                  - Custom
                  - Line
                  - Items
                  - Disassociate
                  - From
                  - Create
                  - Billing
                  - Group
                  - Plan
                  - Rules
                  - Delete
                  - Get
                  - Cost
                  - Reports
                  - Lists
                  - Account
                  - Associations
                  - Reports
                  - Groups
                  - Versions
                  - Items
                  - Plans
                  - Associated
                  - null
                  - Resources
                  - ARN
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/billingconductor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/billingconductor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:billingconductor
  - name: ce
    description: >-
      <p>You can use the Cost Explorer API to programmatically query your cost
      and usage data. You can query for aggregated data such as total monthly
      costs or total daily usage. You can also query for granular data. This
      might include the number of daily write operations for Amazon DynamoDB
      database tables in your production environment. </p> <p>Service
      Endpoint</p> <p>The Cost Explorer API provides the following endpoint:</p>
      <ul> <li> <p> <code>https://ce.us-east-1.amazonaws.com</code> </p> </li>
      </ul> <p>For information about the costs that are associated with the Cost
      Explorer API, see <a
      href="http://aws.amazon.com/aws-cost-management/pricing/">Amazon Web
      Services Cost Management Pricing</a>.</p>
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
            title: ce
          paths:
            /:
              POST:
                summary: UpdateCostCategoryDefinition
                description: >-
                  <p>Updates an existing Cost Category. Changes made to the Cost
                  Category rules will be used to categorize the current month’s
                  expenses and future expenses. This won’t change categorization
                  for the previous m
                tags:
                  - Update
                  - Cost
                  - Categories
                  - Definitions
    overlays:
      - type: APIs.io Search
        url: overlays/ce-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ce-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ce
  - name: devops-guru
    description: >-
      <p> Amazon DevOps Guru is a fully managed service that helps you identify
      anomalous behavior in business critical operational applications. You
      specify the Amazon Web Services resources that you want DevOps Guru to
      cover, then the Amazon CloudWatch metrics and Amazon Web Services
      CloudTrail events related to those resources are analyzed. When anomalous
      behavior is detected, DevOps Guru creates an <i>insight</i> that includes
      recommendations, related events, and related metrics that can help you
      improve your operational applications. For more information, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/welcome.html">What
      is Amazon DevOps Guru</a>. </p> <p> You can specify 1 or 2 Amazon Simple
      Notification Service topics so you are notified every time a new insight
      is created. You can also enable DevOps Guru to generate an OpsItem in
      Amazon Web Services Systems Manager for each insight to help you manage
      and track your work addressing insights. </p> <p> To learn about the
      DevOps Guru workflow, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/welcome.html#how-it-works">How
      DevOps Guru works</a>. To learn about DevOps Guru concepts, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/concepts.html">Concepts
      in DevOps Guru</a>. </p>
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
            title: devops-guru
          paths:
            /channels:
              POST:
                summary: ListNotificationChannels
                description: >-
                  <p> Returns a list of notification channels configured for
                  DevOps Guru. Each notification channel is used to notify you
                  when DevOps Guru generates an insight that contains
                  information about how to improve your operations. The one
                  supported notification channel is Amazon Simple Notification
                  Service (Amazon SNS). </p>
                tags:
                  - Lists
                  - Notifications
                  - Channels
                  - Channels
            /insights/{Id}:
              GET:
                summary: DescribeInsight
                description: >-
                  <p> Returns details about an insight that you specify using
                  its ID. </p>
                tags:
                  - Describe
                  - Insight
                  - Channels
                  - Identifiers
            /accounts/health:
              GET:
                summary: DescribeAccountHealth
                description: >-
                  <p> Returns the number of open reactive insights, the number
                  of open proactive insights, and the number of metrics analyzed
                  in your Amazon Web Services account. Use these numbers to
                  gauge the health of operations in your Amazon Web Services
                  account. </p>
                tags:
                  - Describe
                  - Account
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
            /accounts/overview:
              POST:
                summary: DescribeAccountOverview
                description: >-
                  <p> For the time range passed in, returns the number of open
                  reactive insight that were created, the number of open
                  proactive insights that were created, and the Mean Time to
                  Recover (MTTR) for all closed reactive insights. </p>
                tags:
                  - Describe
                  - Account
                  - Overview
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
            /anomalies/{Id}:
              GET:
                summary: DescribeAnomaly
                description: >-
                  <p> Returns details about an anomaly that you specify using
                  its ID. </p>
                tags:
                  - Describe
                  - Anomaly
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
            /event-sources:
              PUT:
                summary: UpdateEventSourcesConfig
                description: >-
                  <p>Enables or disables integration with a service that can be
                  integrated with DevOps Guru. The one service that can be
                  integrated with DevOps Guru is Amazon CodeGuru Profiler, which
                  can produce proactive recommendations which can be stored and
                  viewed in DevOps Guru.</p>
                tags:
                  - Update
                  - Events
                  - Sources
                  - Configurations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
            /feedback:
              PUT:
                summary: PutFeedback
                description: >-
                  <p> Collects customer feedback about the specified insight.
                  </p>
                tags:
                  - Put
                  - Feedback
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
            /organization/health:
              POST:
                summary: DescribeOrganizationHealth
                description: >-
                  <p>Returns active insights, predictive insights, and resource
                  hours analyzed in last hour.</p>
                tags:
                  - Describe
                  - Organizations
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
            /organization/overview:
              POST:
                summary: DescribeOrganizationOverview
                description: >-
                  <p>Returns an overview of your organization's history based on
                  the specified time range. The overview includes the total
                  reactive and proactive insights.</p>
                tags:
                  - Describe
                  - Organizations
                  - Overview
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
            /organization/health/resource-collection:
              POST:
                summary: DescribeOrganizationResourceCollectionHealth
                description: >-
                  <p>Provides an overview of your system's health. If additional
                  member accounts are part of your organization, you can filter
                  those accounts using the <code>AccountIds</code> field.</p>
                tags:
                  - Describe
                  - Organizations
                  - Resources
                  - Collections
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
            /accounts/health/resource-collection/{ResourceCollectionType}:
              GET:
                summary: DescribeResourceCollectionHealth
                description: >-
                  <p> Returns the number of open proactive insights, open
                  reactive insights, and the Mean Time to Recover (MTTR) for all
                  closed insights in resource collections in your account. You
                  specify the type of Amazon Web Services resources collection.
                  The two types of Amazon Web Services resource collections
                  supported are Amazon Web Services CloudFormation stacks and
                  Amazon Web Services resources that contain the same Amazon Web
                  Services tag. DevOps Guru can be configured to analyze the
                  Amazon Web Services resources that are defined in the stacks
                  or that are tagged using the same tag <i>key</i>. You can
                  specify up to 500 Amazon Web Services CloudFormation stacks.
                  </p>
                tags:
                  - Describe
                  - Resources
                  - Collections
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
            /service-integrations:
              PUT:
                summary: UpdateServiceIntegration
                description: >-
                  <p> Enables or disables integration with a service that can be
                  integrated with DevOps Guru. The one service that can be
                  integrated with DevOps Guru is Amazon Web Services Systems
                  Manager, which can be used to create an OpsItem for each
                  generated insight. </p>
                tags:
                  - Update
                  - Services
                  - Integrations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
            /cost-estimation:
              PUT:
                summary: StartCostEstimation
                description: >-
                  <p>Starts the creation of an estimate of the monthly cost to
                  analyze your Amazon Web Services resources.</p>
                tags:
                  - Start
                  - Cost
                  - Estimation
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
            /resource-collections/{ResourceCollectionType}:
              GET:
                summary: GetResourceCollection
                description: >-
                  <p> Returns lists Amazon Web Services resources that are of
                  the specified resource collection type. The two types of
                  Amazon Web Services resource collections supported are Amazon
                  Web Services CloudFormation stacks and Amazon Web Services
                  resources that contain the same Amazon Web Services tag.
                  DevOps Guru can be configured to analyze the Amazon Web
                  Services resources that are defined in the stacks or that are
                  tagged using the same tag <i>key</i>. You can specify up to
                  500 Amazon Web Services CloudFormation stacks. </p>
                tags:
                  - Get
                  - Resources
                  - Collections
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
            /anomalies/insight/{InsightId}:
              POST:
                summary: ListAnomaliesForInsight
                description: >-
                  <p> Returns a list of the anomalies that belong to an insight
                  that you specify using its ID. </p>
                tags:
                  - Lists
                  - Anomalies
                  - For
                  - Insight
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
            /list-log-anomalies:
              POST:
                summary: ListAnomalousLogGroups
                description: >-
                  <p> Returns the list of log groups that contain log anomalies.
                  </p>
                tags:
                  - Lists
                  - Anomalous
                  - Logs
                  - Groups
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
            /events:
              POST:
                summary: ListEvents
                description: >-
                  <p> Returns a list of the events emitted by the resources that
                  are evaluated by DevOps Guru. You can use filters to specify
                  which events are returned. </p>
                tags:
                  - Lists
                  - Events
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
            /insights:
              POST:
                summary: ListInsights
                description: >-
                  <p> Returns a list of insights in your Amazon Web Services
                  account. You can specify which insights are returned by their
                  start time and status (<code>ONGOING</code>,
                  <code>CLOSED</code>, or <code>ANY</code>). </p>
                tags:
                  - Lists
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
            /monitoredResources:
              POST:
                summary: ListMonitoredResources
                description: >-
                  <p> Returns the list of all log groups that are being
                  monitored and tagged by DevOps Guru. </p>
                tags:
                  - Lists
                  - Monitored
                  - Resources
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
            /organization/insights:
              POST:
                summary: ListOrganizationInsights
                description: >-
                  <p>Returns a list of insights associated with the account or
                  OU Id.</p>
                tags:
                  - Lists
                  - Organizations
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
            /recommendations:
              POST:
                summary: ListRecommendations
                description: >-
                  <p> Returns a list of a specified insight's recommendations.
                  Each recommendation includes a list of related metrics and a
                  list of related events. </p>
                tags:
                  - Lists
                  - Recommendations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
            /channels/{Id}:
              DELETE:
                summary: RemoveNotificationChannel
                description: >-
                  <p> Removes a notification channel from DevOps Guru. A
                  notification channel is used to notify you when DevOps Guru
                  generates an insight that contains information about how to
                  improve your operations. </p>
                tags:
                  - Removes
                  - Notifications
                  - Channels
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
            /insights/search:
              POST:
                summary: SearchInsights
                description: >-
                  <p> Returns a list of insights in your Amazon Web Services
                  account. You can specify which insights are returned by their
                  start time, one or more statuses (<code>ONGOING</code> or
                  <code>CLOSED</code>), one or more severities
                  (<code>LOW</code>, <code>MEDIUM</code>, and
                  <code>HIGH</code>), and type (<code>REACTIVE</code> or
                  <code>PROACTIVE</code>). </p> <p> Use the <code>Filters</code>
                  parameter to specify status and severity search parameters.
                  Use the <code>Type</code> parameter to specify
                  <code>REACTIVE</code> or <code>PROACTIVE</code> in your
                  search. </p>
                tags:
                  - Search
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
            /organization/insights/search:
              POST:
                summary: SearchOrganizationInsights
                description: >-
                  <p> Returns a list of insights in your organization. You can
                  specify which insights are returned by their start time, one
                  or more statuses (<code>ONGOING</code>, <code>CLOSED</code>,
                  and <code>CLOSED</code>), one or more severities
                  (<code>LOW</code>, <code>MEDIUM</code>, and
                  <code>HIGH</code>), and type (<code>REACTIVE</code> or
                  <code>PROACTIVE</code>). </p> <p> Use the <code>Filters</code>
                  parameter to specify status and severity search parameters.
                  Use the <code>Type</code> parameter to specify
                  <code>REACTIVE</code> or <code>PROACTIVE</code> in your
                  search. </p>
                tags:
                  - Search
                  - Organizations
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
            /resource-collections:
              PUT:
                summary: UpdateResourceCollection
                description: >-
                  <p> Updates the collection of resources that DevOps Guru
                  analyzes. The two types of Amazon Web Services resource
                  collections supported are Amazon Web Services CloudFormation
                  stacks and Amazon Web Services resources that contain the same
                  Amazon Web Services tag. DevOps Guru can be configured to
                  analyze the Amazon Web Services resources that are defined in
                  the stacks or that are tagged using the same tag <i>key</i>.
                  You can specify up to 500 Amazon Web Services CloudFormation
                  stacks. This method also creates the IAM role required for you
                  to use DevOps 
                tags:
                  - Update
                  - Resources
                  - Collections
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
                  - Collections
    overlays:
      - type: APIs.io Search
        url: overlays/devops-guru-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/devops-guru-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:devops-guru
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---