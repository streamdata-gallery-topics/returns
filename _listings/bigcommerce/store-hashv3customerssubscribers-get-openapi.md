---
swagger: "2.0"
x-collection-name: BigCommerce
x-complete: 0
info:
  title: BigCommerce Returns all newsletter subscribers
  description: Returns a paginated Subscribers collection.
  version: 1.0.0
host: api.bigcommerce.com
basePath: /stores
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{store_hash}/v3/catalog/summary:
    get:
      summary: Returns a lightweight inventory summary
      description: Returns a lightweight inventory summary from the BigCommerce Catalog.
      operationId: V3CatalogSummaryByStoreHashGet
      x-api-path-slug: store-hashv3catalogsummary-get
      parameters:
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Returns
      - Lightweight
      - Inventory
      - Summary
  /{store_hash}/v3/customers/subscribers:
    get:
      summary: Returns all newsletter subscribers
      description: Returns a paginated Subscribers collection.
      operationId: V3CustomersSubscribersByStoreHashGet
      x-api-path-slug: store-hashv3customerssubscribers-get
      parameters:
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Returns
      - ""
      - Newsletter
      - Subscribers
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