---
name: Creates
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/creates.png
url: https://example.com/apis/creates.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Creates
apis:
  - name: Adyen Test Cards API
    description: >-
      The Test Cards API provides endpoints for generating custom test card
      numbers. For more information, refer to [Custom test
      cards](https://docs.adyen.com/development-resources/testing/create-test-cards)
      documentation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/development-resources/testing/create-test-cards
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/development-resources/testing/create-test-cards
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Test Cards API
            x-timestamp: '2022-05-03T09:24:07Z'
          x-groups:
            - General
          tags:
            - name: General
          paths:
            /createTestCardRanges:
              post:
                tags:
                  - Creates
                  - One
                  - Or
                  - More
                  - Tests
                  - Cards
                  - Ranges
                  - Tests
                  - Cards
                  - Ranges
                summary: Creates one or more test card ranges.
                description: null
    overlays:
      - type: APIs.io Search
        url: overlays/test-cards-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/test-cards-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-test-cards-api
  - name: FactSet Vermilion API
    description: >-
      The Vermilion API, enables users to programmatically access FactSet's
      Vermilion Reporting Suite (VRS) and seamlessly integrate into customer's
      3rd party applications. The API is referred to as two key product
      initiatives, the REST API and the SCIM API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/vermilion-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/vermilion-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/vermilion-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/vermilion-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/vermilion-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/vermilion-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: VRS API documentation
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/vermilion-api
          tags:
            - name: Datasource
            - name: Entities
            - name: Reports
            - name: Report instance
            - name: SCIM
          paths:
            /v1/{tenant}/data-sources:
              get:
                tags:
                  - Lists
                  - All
                  - Datasources
                  - V1
                  - Tenant
                  - Data
                  - Sources
                summary: Lists all datasources
                description: List all datasources the user has permission to see
            /v1/{tenant}/data-sources/{dataSourceCode}:
              get:
                tags:
                  - Gets
                  - Datasource
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                summary: Gets a datasource
                description: Gets a datasource based on the code passed
            /v1/{tenant}/data-sources/{dataSourceCode}/data:
              get:
                tags:
                  - Gets
                  - The
                  - Data
                  - For
                  - Datasource
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                summary: Gets the data for the datasource
                description: >-
                  Gets the data for the datasource. There are optional query
                  parameters to filter the data
            /v1/{tenant}/entities/{entityCode}/values:
              get:
                tags:
                  - Gets
                  - The
                  - Entity
                  - Values
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                summary: Gets the entity values
                description: Gets the entity values for the specified entity
            /v1/{tenant}/reports:
              get:
                tags:
                  - Gets
                  - All
                  - Report
                  - Definitions
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                summary: Gets all report definitions
                description: Gets all report definitions the user has permissions for
            /v1/{tenant}/reports/{reportDefinitionCode}:
              get:
                tags:
                  - Gets
                  - Report
                  - Definition
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                summary: Gets a report definition
                description: Gets a report defintion based on the code specified
            /v1/report-instances/generate:
              post:
                tags:
                  - Generates
                  - Report
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                summary: Generates a report
                description: >-
                  Generates a report using the specified ID and the JSON in the
                  request body
            /v1/{tenant}/report-instances/{reportInstanceId}:
              delete:
                tags:
                  - Cancels
                  - Report
                  - Generation
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Cancels a report generation
                description: >-
                  Sends a request to cancel a report generation based on the
                  report instance id passed
              get:
                tags:
                  - Gets
                  - Report
                  - Instance
                  - Based
                  - 'On'
                  - The
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Gets a report instance based on the ID
                description: Gets a report instance object based on the ID passed
            /v1/{tenant}/report-instances:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Report
                  - Instances
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Gets a list of report instances
                description: >-
                  Gets a list of report instances. This can be filtered down
                  further by including query parameters in the URL. For example,
                  a report definition id can be added so the only report
                  instances returned are the ones with a matching id
            /v1/{tenant}/report-instances/{reportInstanceId}/results/{reportFileName}:
              get:
                tags:
                  - Gets
                  - The
                  - Generated
                  - File
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                summary: Gets the generated file
                description: >-
                  Get the generated file for a report instance. Users can fetch
                  the generated report once the genration is finished. The
                  report instance id and the report file name are passed in as
                  path paramters
            /v1/{tenant}/report-instances/{reportInstanceId}/logs:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Logs
                  - For
                  - The
                  - Report
                  - Instance
                  - Generation
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                summary: Gets a list of logs for the report instance generation
                description: >-
                  Gets a list of logs for the generated report instance. Allows
                  the user to sort on log message, type and date. Also allows
                  for retrieving of just the errors & warnings'
            /scim/v2/Users:
              get:
                tags:
                  - Retrieves
                  - List
                  - Of
                  - Users
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                summary: Retrieves a list of VRS users
                description: Retrieves a list of VRS users
              post:
                tags:
                  - Creates
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                summary: Creates a user
                description: Creates a VRS user
            /scim/v2/Users/{userId}:
              get:
                tags:
                  - Retrieves
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Retrieves a VRS User
                description: Retrieves a VRS user based on their ID
              delete:
                tags:
                  - Deletes
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Deletes a VRS user
                description: >-
                  Deletes a VRS user (this marks them as 'Deleted' in the
                  database)
              patch:
                tags:
                  - Add
                  - Or
                  - Remove
                  - User
                  - Attributes
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Add or remove VRS user attributes
                description: >-
                  Adds or removes VRS user attributes based on the JSON
                  properties
              put:
                tags:
                  - Updates
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Updates a VRS user
                description: Updates (replaces) a VRS user with the properties in the JSON
            /scim/v2/Groups:
              get:
                tags:
                  - Retrieves
                  - List
                  - Of
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                summary: Retrieves a list of VRS role
                description: Retrieves a VRS roles
              post:
                tags:
                  - Creates
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                summary: Creates a role
                description: Creates a VRS role
            /scim/v2/Groups/{groupId}:
              get:
                tags:
                  - Retrieves
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Retrieves a VRS role
                description: Retrieves a VRS role based on the ID
              delete:
                tags:
                  - Deletes
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Deletes a VRS role
                description: Deletes a VRS role
              patch:
                tags:
                  - Add
                  - Or
                  - Remove
                  - User
                  - To/from
                  - Group
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Add or remove a user to/from a group
                description: Adds or removes a VRS user to/from a VRS role
              put:
                tags:
                  - Updates
                  - Group
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Updates a VRS Group
                description: Updates (replaces) a VRS Group with the pr
    overlays:
      - type: APIs.io Search
        url: overlays/vermilion-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/vermilion-openapi-api-evangelist-ratings.yml
    aid: factset:factset-vermilion-api
  - name: FactSet Issue Tracker API
    description: >-
      Through Issue Tracker API, Clients can Create, Read and Update the Issue
      Tracker Issues programmatically.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/issue-tracker-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/issue-tracker-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/issue-tracker-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/issue-tracker-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/issue-tracker-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/issue-tracker-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Issue Tracker API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          tags:
            - name: Issue
              description: Updating and retrieving issue data within the Issue Tracker
          paths:
            /issues:
              post:
                summary: Creates a Issue Tracker issue
                tags:
                  - Creates
                  - Issue
                  - Tracker
                  - Issues
                description: Creates a new issue in Issue Tracker
            /issues/{id}:
              get:
                summary: Get the matched issue details
                tags:
                  - Get
                  - The
                  - Matched
                  - Issue
                  - Details
                  - Issues
                  - Id
                description: >-
                  Retrieve the information of the client with the matching issue
                  Id.
            /issues/{id}/comments:
              post:
                summary: post comment to Issue Tracker issue
                tags:
                  - Issue
                  - Tracker
                  - Issues
                  - Id
                  - Comments
                description: 'Reply to the existing matched issue '
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catal
    overlays:
      - type: APIs.io Search
        url: overlays/issue-tracker-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/issue-tracker-openapi-api-evangelist-ratings.yml
    aid: factset:factset-issue-tracker-api
  - name: FactSet StreetAccount News API
    description: >-
      Accessing streetAccount news along with business logic contained in the
      workstation experience
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/streetaccount-news-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/streetaccount-news-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/streetaccount-news-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/streetaccount-news-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/streetaccount-news-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/streetaccount-news-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: StreetAccount News API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          tags:
            - name: Filters
              description: Get flattened or structured filters
            - name: Headlines
              description: Get headlines for a specified view or specified filters
            - name: Views
              description: Create, edit and delete views
            - name: StreetAccount Historical Stories
              description: Request, check the status and download the XML files.
          paths:
            /streetaccount/headlines:
              post:
                summary: Retrieve StreetAccount headlines for given filters
                description: >-
                  This endpoint will pull all headlines produced by
                  StreetAccount and the full story body will be returned by the
                  data set. Filters can be specified via the endpoint below.
                tags:
                  - Retrieve
                  - Street
                  - Account
                  - Headlines
                  - For
                  - Given
                  - Filters
                  - Streetaccount
                  - Headlines
            /streetaccount/views/{id}/headlines:
              post:
                summary: Retrieve StreetAccount headlines for given view
                description: >-
                  This endpoint allows you to pull all headlines produced by
                  StreetAccount for a saved view. The full story body will be
                  returned by the data set. Views can be created via the ‘Create
                  Views’ endpoint.
                tags:
                  - Retrieve
                  - Street
                  - Account
                  - Headlines
                  - For
                  - Given
                  - View
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
            /streetaccount/views:
              get:
                summary: Retrieves StreetAccount search views
                description: >-
                  This endpoint allows you to pull the full list of
                  StreetAccount views that have been previously saved.
                tags:
                  - Retrieves
                  - Street
                  - Account
                  - Search
                  - Views
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
            /streetaccount/views/{id}:
              post:
                summary: Creates and saves a StreetAccount view
                description: >-
                  This endpoint allows you to create a new StreetAccount view.
                  Select watchlists/tickers and filters of your choice to create
                  and save a view.
                tags:
                  - Creates
                  - And
                  - Saves
                  - Street
                  - Account
                  - View
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
              put:
                summary: Edits and saves an existing StreetAccount view
                description: >-
                  This endpoint allows you to edit the criteria used for a
                  previously saved StreetAccount view.
                tags:
                  - Edits
                  - And
                  - Saves
                  - An
                  - Existing
                  - Street
                  - Account
                  - View
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
              delete:
                summary: Deletes an existing StreetAccount view
                description: >-
                  This endpoint allows you to delete a previously saved
                  StreetAccount view.
                tags:
                  - Deletes
                  - An
                  - Existing
                  - Street
                  - Account
                  - View
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
            /streetaccount/filters:
              get:
                summary: Retrieve all StreetAccount filters
                tags:
                  - Retrieve
                  - All
                  - Street
                  - Account
                  - Filters
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
                  - Filters
                description: >-
                  Add StreetAccount filters (watchlists, company filters, market
                  topics, regions and sectors) to filter down StreetAccount
                  headlines by the relevant categories. Set the structured
                  and/or flattened flag. If structured flag is set, parent and
                  child filter information will be returned. If flattened flag
                  is set, flattened filters will be returned which can be used
                  with the headlines and createView endpoints. Both flags can be
                  set to return both sets of filters.  If no params are provided
                  it will return both
            /streetaccount/historical/request-files:
              get:
                tags:
                  - Returns
                  - The
                  - Job
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
                  - Filters
                  - Historical
                  - Request
                  - Files
                summary: Returns the jobID
                description: >-
                  Give the startDate and endDate parameters as request
                  parameters in the /request-files endpoint, it returns the
                  jobID. startDate and endDate should be in YYYY-MM-DDTHH:MM:SSZ
                  format. This API only supports adhoc requests to retrieve
                  historical files and does not support real-time files and if
                  you interested in require real-time push should consider the
                  other three methods (pushed via SFTP, to QNT account, or your
                  Azure Storage). Per API request able to query till 2 years of
                  data
            /streetaccount/historical/check-status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - And
                  - Percentage
                  - Of
                  - Completion
                  - For
                  - Requested
                  - Job
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
                  - Filters
                  - Historical
                  - Request
                  - Files
                  - Check
                  - Status
                summary: >-
                  Returns the status and percentage of completion for the
                  requested jobID
                description: >-
                  Need to plug-in the jobID from /request-files into
                  /check-status endpoint
            /streetaccount/historical/get-files:
              get:
                tags:
                  - Returns
                  - The
                  - Street
                  - Account
                  - Files
                  - For
                  - Specified
                  - Date
                  - Range
                  - Streetaccount
                  - Headlines
                  - Views
                  - Id
                  - Filters
                  - Historical
                  - Request
                  - Files
                  - Check
                  - Status
                  - Get
                summary: >-
                  Returns the StreetAccount XML files for the specified date
                  range
                description: >-
                  Need to plug-in the jobID from /check-status into /get-files
                  endpoint
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/stre
    overlays:
      - type: APIs.io Search
        url: overlays/streetaccount-news-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/streetaccount-news-openapi-api-evangelist-ratings.yml
    aid: factset:factset-streetaccount-news-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---