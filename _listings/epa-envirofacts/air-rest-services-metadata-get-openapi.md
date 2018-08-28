---
swagger: "2.0"
x-collection-name: EPA Envirofacts
x-complete: 0
info:
  title: U.S. EPA Enforcement and Compliance History Online (ECHO) - Clean Air Act
    Clean Air Act Metadata Service
  description: Returns the JSON Object Name and ColumnId for usage with the qcolumns
    parameter for get_qid, get_facility_info and other service endpoints.
  contact:
    name: US EPA, OECA Integration, Targeting and Access Branch
  version: 0.0.0
host: ofmpub.epa.gov
basePath: /echo
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /air_rest_services.get_facility_info:
    get:
      summary: Clean Air Act Facility Enhanced Search
      description: Returns either an array of Facilities or an array of Clusters that
        meet the specified search criteria.
      operationId: returns-either-an-array-of-facilities-or-an-array-of-clusters-that-meet-the-specified-search-criteri
      x-api-path-slug: air-rest-services-get-facility-info-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: output
        description: Output Format Flag
      responses:
        200:
          description: OK
      tags:
      - Environment
      - Clean
      - Air
      - Act
      - Facility
      - Enhanced
      - Search
  /air_rest_services.metadata:
    get:
      summary: Clean Air Act Metadata Service
      description: Returns the JSON Object Name and ColumnId for usage with the qcolumns
        parameter for get_qid, get_facility_info and other service endpoints.
      operationId: returns-the-json-object-name-and-columnid-for-usage-with-the-qcolumns-parameter-for-get-qid-get-faci
      x-api-path-slug: air-rest-services-metadata-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: output
        description: Output Format Flag
      responses:
        200:
          description: OK
      tags:
      - Environment
      - Clean
      - Air
      - Act
      - Metadata
      - Service
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---