---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 1
info:
  title: RingCentral Connect Platform API Explorer
  description: this-is-an-interactive-api-explorer-for-the-ringcentral-connect-platform--to-use-this-service-you-will-need-to-have-a-developer-account---links--a-hrefhttpsnetstorage-ringcentral-comdpwapiexplorerrcplatform-basic-ymlv20180514092722-target-blankringcentral-api-specaspannbspnbspopenapi-fka-swagger-formatnbspnbspnbspnbspspana-hrefhttpsgithub-comoaiopenapispecification-target-blanklearn-more-about-openapia
  version: 1.0.0
host: platform.ringcentral.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/business-hours:
    get:
      summary: Get User Business Hours
      description: "Returns the extension user hours when answering rules are to be
        applied.\nApp Permission\nReadAccounts\nUser Permission\nReadExtensions\nUsage
        Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadAccounts] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [ReadUserAnsweringRules]
        permission for requested resource.\n\n\n404\nCMN-102\nResource for parameter
        [extensionId] is not found"
      operationId: loadUserBusinessHours
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidbusinesshours-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - User
      - Business
      - Hours
    put:
      summary: Update User Business Hours
      description: "Updates the extension user hours when answering rules are to be
        applied.\nApp Permission\nEditExtensions\nUser Permission\nEditUserAnsweringRules\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [ranges] value is invalid\n\n\n403\nCMN-401\nIn
        order to call this API endpoint, application needs to have [EditExtensions]
        permission\n\n\n404\nCMN-102\nResource for parameter [extensionId] is not
        found"
      operationId: updateUserBusinessHours
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidbusinesshours-put
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: body
        name: body
        description: JSON body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - User
      - Business
      - Hours
  /restapi/v1.0/account/{accountId}/business-hours:
    get:
      summary: Get Company Business Hours
      description: |-
        Returns company hours when answering rules are to be applied.
        App Permission
        ReadAccounts
        User Permission
        ReadUserAnsweringRules
        Usage Plan Group
        Light
      operationId: loadBusinesshoursInfo
      x-api-path-slug: restapiv1-0accountaccountidbusinesshours-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - Company
      - Business
      - Hours
    put:
      summary: Update Company Business Hours
      description: "Updates company hours when answering rules are to be applied.\nApp
        Permission\nEditExtensions\nUser Permission\nEditUserAnsweringRules\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nAWR-176\nAt least one time range for [monday] required\n\n\n400\nAWR-177\nTime
        ranges limit for [monday] exceeded\n\n\n400\nCMN-101\nParameter [schedule.weeklyRanges]
        value is invalid"
      operationId: updateCompanyBusinessHours
      x-api-path-slug: restapiv1-0accountaccountidbusinesshours-put
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: body
        name: body
        description: JSON body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Company
      - Business
      - Hours
---