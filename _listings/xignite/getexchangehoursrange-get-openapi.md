---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Global Holidays Get Exchange Hours Range
  description: Get exchange hours range.
  version: 1.0.0
host: globalholidays.xignite.com
basePath: xGlobalHolidays.json/XigniteGlobalHolidays
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetExchangeHours:
    get:
      summary: Get Exchange Hours
      description: Get exchange hours.
      operationId: GetExchangeHours
      x-api-path-slug: getexchangehours-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Exchange
      - Hours
  /GetExchangeHoursRange:
    get:
      summary: Get Exchange Hours Range
      description: Get exchange hours range.
      operationId: GetExchangeHoursRange
      x-api-path-slug: getexchangehoursrange-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Exchange
      - Hours
      - Range
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