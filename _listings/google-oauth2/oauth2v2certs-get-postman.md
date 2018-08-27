{
  "info": {
    "name": "Google OAuth2 APIs Get Certificate",
    "_postman_id": "56731078-3a5b-4e85-a9f1-48d1da4666ae",
    "description": "Get the certification for this session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Certificate",
      "item": [
        {
          "id": "4db72f15-3865-4c28-b40a-697060cb791c",
          "name": "oauth2.getCertForOpenIdConnect",
          "request": {
            "url": "http://www.googleapis.com/oauth2/v2/certs",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get the certification for this session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8d070ff-c48f-44a3-a348-ad9d7f653693"
            }
          ]
        }
      ]
    }
  ]
}