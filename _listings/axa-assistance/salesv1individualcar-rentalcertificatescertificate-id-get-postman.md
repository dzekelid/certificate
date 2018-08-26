{
  "info": {
    "name": "AXA Assistance Gets the car rental certificate details.",
    "_postman_id": "2ed332de-fc54-48bb-8dee-905e3e6a1954",
    "description": "Gets the car rental certificate details.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "e7b8f341-3265-40aa-817f-8b657bdf95fb",
          "name": "getSalesV1IndividualCar_rentalCertificatesCertificate_id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "sandbox.api.axa-assistance.com",
              "path": [
                "sales/v1/individual/car_rental/certificates/:certificate_id"
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
            "description": "Gets the car rental certificate details"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4cae4831-59d1-44c7-81e1-c3424e9bbe91"
            }
          ]
        }
      ]
    }
  ]
}