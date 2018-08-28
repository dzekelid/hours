---
swagger: "2.0"
x-collection-name: Clover
x-complete: 0
info:
  title: Clover Get a list this merchant opening hours
  version: 1.0.0
  description: Get a list this merchant opening hours.
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/opening_hours:
    get:
      summary: Get a list this merchant opening hours
      description: Get a list this merchant opening hours.
      operationId: GetAllMerchantOpeningHours
      x-api-path-slug: v3merchantsmidopening-hours-get
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Opening
      - Hours
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