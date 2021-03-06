---
swagger: "2.0"
x-collection-name: Logicbroker
x-complete: 0
info:
  title: Logic Broker CommerceAPI Returns the invoice with the specified key.
  version: 1.0.0
  description: Request rate limited to 10 requests per second with bursts up to 100
    requests.
host: stage.commerceapi.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/Returns:
    get:
      summary: Search returns
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Return_SearchReturns
      x-api-path-slug: apiv1returns-get
      parameters:
      - in: query
        name: filters.advanced
        description: Advanced query options
      - in: query
        name: filters.from
        description: Beginning of time search window
      - in: query
        name: filters.linkkey
        description: The linkkey identifies a group of related documents
      - in: query
        name: filters.page
        description: Page number
      - in: query
        name: filters.pageSize
        description: Page size
      - in: query
        name: filters.partnerPO
        description: The partners purchase order number
      - in: query
        name: filters.receiverCompanyId
        description: This Id is indicate who is received this document
      - in: query
        name: filters.senderCompanyId
        description: This Id is indicate who is sent this document
      - in: query
        name: filters.sourceKey
        description: Source key is usually the unique key the sender uses to find
          this document
      - in: query
        name: filters.status
        description: The status of the document
      - in: query
        name: filters.to
        description: End of time search window
      responses:
        200:
          description: OK
      tags:
      - Search
      - Returns
  /api/v1/Returns/CustomXML:
    post:
      summary: Create return(s) based on custom XML.
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Return_UploadCustomXml
      x-api-path-slug: apiv1returnscustomxml-post
      parameters:
      - in: body
        name: data
        description: XML data to upload
        schema:
          $ref: '#/definitions/holder'
      - in: formData
        name: file
        description: File to upload
      - in: query
        name: xmlType
        description: XML type, leave blank unless directed otherwise
      responses:
        200:
          description: OK
      tags:
      - Return(s)
      - Based
      - "On"
      - Custom
      - XML
  /api/v1/Invoices/{LogicbrokerKey}:
    get:
      summary: Returns the invoice with the specified key.
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Invoice_GetInvoice
      x-api-path-slug: apiv1invoiceslogicbrokerkey-get
      parameters:
      - in: path
        name: LogicbrokerKey
        description: The logicbroker key to search for
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Invoice
      - Specified
      - Key
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