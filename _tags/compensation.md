---
name: Compensation
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/compensation.png
url: https://example.com/apis/compensation.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Compensation
apis:
  - name: FactSet People API
    description: >-
      Fetch People Profiles, Job History, or get associated positions and names
      of companies.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-people-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-people-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-people-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-people-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-people-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-people-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet People API
          tags:
            - name: Profiles
              description: >-
                Return information about the person with the specified entity
                ID.
            - name: Job History
              description: Returns the job history of the person
            - name: Company
              description: Returns a list of associated people for a requested company
          paths:
            /factset-people/v1/profiles:
              get:
                summary: >-
                  Return information about the person with the specified entity
                  ID.
                description: >
                  Returns a summary of basic information about the person
                  referenced by the entityId specified in the URI.
                tags:
                  - Return
                  - Information
                  - About
                  - The
                  - Person
                  - With
                  - Specified
                  - Entity
                  - D.
                  - Factset
                  - People
                  - V1
                  - Profiles
              post:
                summary: Returns profile information for a large list of people.
                tags:
                  - Returns
                  - Profile
                  - Information
                  - For
                  - Large
                  - List
                  - Of
                  - People.
                  - Factset
                  - People
                  - V1
                  - Profiles
            /factset-people/v1/jobs:
              get:
                summary: Returns the Job history of the person.
                description: >
                  Returns the `Job` history of the person referenced by the
                  entityId specified in the request.
                tags:
                  - Returns
                  - The
                  - Job
                  - History
                  - Of
                  - Person.
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
              post:
                summary: Returns the Job history for the large list of people.
                description: >
                  Returns the `Job` history of the person referenced by the
                  entityId specified in the request.
                tags:
                  - Returns
                  - The
                  - Job
                  - History
                  - For
                  - Large
                  - List
                  - Of
                  - People.
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
            /factset-people/v1/company-people:
              get:
                summary: >-
                  Returns the list of people for the specified company
                  identifiers
                description: >
                  Returns the list of executives associated the company
                  identifier requested. Information includes the job functions,
                  email, phone, title, name, and FactSet Entity Identifier. The
                  personId returned can then be used in the `/profiles` endpoint
                  to learn more about the given person.
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - People
                  - For
                  - Specified
                  - Company
                  - Identifiers
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
              post:
                summary: >-
                  Returns the list of people associated for a large list of
                  company identitifers
                description: >
                  Returns the list of executives associated the company
                  identifier requested. Information includes the job functions,
                  email, phone, title, name, and FactSet Entity Identifier. The
                  personId returned can then be used in the /profiles endpoint
                  to learn more about the given person.
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - People
                  - Associated
                  - For
                  - Large
                  - Company
                  - Identitifers
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
            /factset-people/v1/company-positions:
              get:
                summary: >-
                  Returns the list of people for the specified company
                  identifiers and position
                description: >
                  Returns the list of people, name, and title for a list of
                  company ids and requested position. Positions include-
                    * Chairman
                    * Chief Executive Officer
                    * President
                    * Chief Operating Officer
                    * Chief Financial Officer
                    * Chief Technology Officer
                    * Chief Investment Officer
                    * Founder(s)
                    * Compliance Officer
                    * Admin
                    * Independent Director
                    * Directors/Board Members
                    * Investor Relations
                    * Legal Counsel
                    * Treasurer
                    * Sales and Marketing Managers
                    * Human Resources
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - People
                  - For
                  - Specified
                  - Company
                  - Identifiers
                  - And
                  - Position
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
                  - Positions
              post:
                summary: >-
                  Returns the list of people associated for a large list of
                  company identitifers and position
                description: >
                  Returns the list of people, name, and title for a list of
                  company ids and requested position. Positions include-
                    * Chairman
                    * Chief Executive Officer
                    * President
                    * Chief Operating Officer
                    * Chief Financial Officer
                    * Chief Technology Officer
                    * Chief Investment Officer
                    * Founder(s)
                    * Compliance Officer
                    * Admin
                    * Independent Director
                    * Directors/Board Members
                    * Investor Relations
                    * Legal Counsel
                    * Treasurer
                    * Sales and Marketing Managers
                    * Human Resources
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - People
                  - Associated
                  - For
                  - Large
                  - Company
                  - Identitifers
                  - And
                  - Position
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
                  - Positions
            /factset-people/v1/company-compensation:
              get:
                summary: >-
                  Returns the compensation details of the people for the
                  specified company identifier
                description: >-
                  Returns the list of company-level executive compensation data
                  items for the top executives listed in annual filings.The
                  coverage of the compensation details for the executives are
                  limited to US region. All the compensation figures are
                  expressed in raw units. 
                tags:
                  - Returns
                  - The
                  - Compensation
                  - Details
                  - Of
                  - People
                  - For
                  - Specified
                  - Company
                  - Identifier
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
                  - Positions
                  - Compensation
              post:
                summary: >-
                  Returns the compensation details for the people for the
                  specified company identifier
                description: >-
                  Returns the list of company-level executive compensation data
                  items for the top executives listed in annual filings for the
                  most recent fiscal year. The coverage of the compensation
                  details for the executives are limited to US region. All the
                  compensation figures are expressed in raw units. 
                tags:
                  - Returns
                  - The
                  - Compensation
                  - Details
                  - For
                  - People
                  - Specified
                  - Company
                  - Identifier
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
                  - Positions
                  - Compensation
            /factset-people/v1/company-stats:
              get:
                summary: Returns statistics about top leadership of a company.
                description: >
                  Returns the statistics such as the average age, tenure,
                  compensation of leadership, number of executives, and the
                  gender diversity of leadership. We can utilize the data for
                  analyzing a company's board and management.
                tags:
                  - Returns
                  - Statistics
                  - About
                  - Top
                  - Leadership
                  - Of
                  - Company.
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
                  - Positions
                  - Compensation
                  - Stats
              post:
                summary: Returns statistics about top leadership of a company.
                description: >-
                  Returns the statistics such as the average age, tenure,
                  compensation of leadership, number of executives, and the
                  gender diversity of leadership. We can utilize the data for
                  analyzing a company's board and management. 
                tags:
                  - Returns
                  - Statistics
                  - About
                  - Top
                  - Leadership
                  - Of
                  - Company.
                  - Factset
                  - People
                  - V1
                  - Profiles
                  - Jobs
                  - Company
                  - Positions
                  - Compensation
                  - Sta
    overlays:
      - type: APIs.io Search
        url: overlays/people-openapi-original.yml
      - type: APIs.io Search
        url: overlays/people-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/people-openapi-api-evangelist-ratings.yml
    aid: factset:factset-people-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---