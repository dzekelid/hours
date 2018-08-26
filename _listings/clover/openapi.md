---
swagger: "2.0"
x-collection-name: Clover
x-complete: 1
info:
  title: ""
  version: 1.0.0
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
    post:
      summary: Create a set of merchant opening hours
      description: Create a set of merchant opening hours.
      operationId: CreateMerchantOpeningHours
      x-api-path-slug: v3merchantsmidopening-hours-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
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
  /v3/merchants/{mId}/opening_hours/{hId}:
    get:
      summary: Get a specific set of merchant opening hours
      description: Get a specific set of merchant opening hours.
      operationId: GetMerchantOpeningHours
      x-api-path-slug: v3merchantsmidopening-hourshid-get
      parameters:
      - in: path
        name: hId
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
      - HId
    post:
      summary: Update a set of merchant opening hours
      description: Update a set of merchant opening hours.
      operationId: UpdateMerchantOpeningHours
      x-api-path-slug: v3merchantsmidopening-hourshid-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: hId
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
      - HId
    delete:
      summary: Delete a set of merchant opening hours
      description: Delete a set of merchant opening hours.
      operationId: DeleteMerchantOpeningHours
      x-api-path-slug: v3merchantsmidopening-hourshid-delete
      parameters:
      - in: path
        name: hId
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
      - HId
---