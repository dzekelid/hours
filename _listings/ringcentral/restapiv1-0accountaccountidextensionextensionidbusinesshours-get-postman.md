{
  "info": {
    "name": "RingCentral Get User Business Hours",
    "_postman_id": "13938ea9-3ab9-40a7-baa9-798ef9513c73",
    "description": "Returns the extension user hours when answering rules are to be applied.\nApp Permission\nReadAccounts\nUser Permission\nReadExtensions\nUsage Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint, application needs to have [ReadAccounts] permission\n\n\n403\nCMN-408\nIn order to call this API endpoint, user needs to have [ReadUserAnsweringRules] permission for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId] is not found",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "0b6a6b04-2898-402c-8e93-ee396e43b906",
          "name": "loadUserBusinessHours",
          "request": {
            "url": {
              "protocol": "http",
              "host": "platform.ringcentral.com",
              "path": [
                "restapi/v1.0/account/:accountId/extension/:extensionId/business-hours"
              ],
              "variable": [
                {
                  "id": "accountId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "extensionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the extension user hours when answering rules are to be applied.\nApp Permission\nReadAccounts\nUser Permission\nReadExtensions\nUsage Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint, application needs to have [ReadAccounts] permission\n\n\n403\nCMN-408\nIn order to call this API endpoint, user needs to have [ReadUserAnsweringRules] permission for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId] is not found"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "77843fab-234a-4886-81be-432cf8947ee6"
            }
          ]
        }
      ]
    }
  ]
}