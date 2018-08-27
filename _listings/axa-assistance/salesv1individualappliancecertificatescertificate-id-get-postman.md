{
  "info": {
    "name": "AXA Assistance Get appliance (Extended warranty, purchase insurance ) certificate details.",
    "_postman_id": "c6517e65-a891-4391-9b6f-399bb8e01608",
    "description": "Get appliance (Extended warranty, purchase insurance ) certificate details.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "3a812e2c-4442-4d32-9a8d-1322aec5ed72",
          "name": "getSalesV1IndividualApplianceCertificatesCertificate_id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "sandbox.api.axa-assistance.com",
              "path": [
                "sales/v1/individual/appliance/certificates/:certificate_id"
              ],
              "variable": [
                {
                  "id": "certificate_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "accept-language",
                "value": "{}",
                "description": "Accepted language, IANA language codification",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get appliance (Extended warranty, purchase insurance ) certificate details"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "74d0b14e-7786-44c4-8034-1e09574a8a0d"
            }
          ]
        }
      ]
    }
  ]
}