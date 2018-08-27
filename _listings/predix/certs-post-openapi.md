---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Enterprise Connect Request a digital certificate
  description: Submit a CSR for a certificate for the EC usage
  version: 1.0.0
host: ec-predix-service-osaka.run.aws-usw02-pr.ice.predix.io
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /certs:
    post:
      summary: Request a digital certificate
      description: Submit a CSR for a certificate for the EC usage
      operationId: submit-a-csr-for-a-certificate-for-the-ec-usage
      x-api-path-slug: certs-post
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: body
        name: content
        description: The CSR content in pem format
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: predix-zone-id
        description: Cloud Foundry service instance id
      responses:
        200:
          description: Successful response
      tags:
      - Request
      - Digital
      - Certificate
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