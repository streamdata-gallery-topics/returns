---
swagger: "2.0"
x-collection-name: AWS Database Migration Service
x-complete: 0
info:
  title: AWS Database Migration Service API Describe Endpoints
  version: 1.0.0
  description: Returns information about the endpoints for your account in the current
    region.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeEndpoints:
    get:
      summary: Describe Endpoints
      description: Returns information about the endpoints for your account in the
        current region.
      operationId: describeEndpoints
      x-api-path-slug: actiondescribeendpoints-get
      parameters:
      - in: query
        name: Filters
        description: Filters applied to the describe action
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous      request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Endpoints
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