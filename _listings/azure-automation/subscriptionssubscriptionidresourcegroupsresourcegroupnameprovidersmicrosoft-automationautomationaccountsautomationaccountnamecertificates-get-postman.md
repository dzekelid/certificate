{
  "info": {
    "name": "Azure Automation API Certificate List By Automation Account",
    "_postman_id": "2e43d089-92fd-4aea-b9cd-e6f0896eb336",
    "description": "Retrieve a list of certificates.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "certificate",
      "item": [
        {
          "id": "84e6f194-cf97-48c4-8dcc-9ee7eb6c8b3f",
          "name": "Certificate_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/certificates"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "automationAccountName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "resourceGroupName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a list of certificates"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d4f9e863-6793-49bf-9aa1-82123812e0a6"
            }
          ]
        }
      ]
    }
  ]
}