swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
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
    get:
      summary: Retrieve current certificate
      description: Retrieve the current certificate issued by the GE Digital CA.
      operationId: retrieve-the-current-certificate-issued-by-the-ge-digital-ca
      x-api-path-slug: certs-get
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: header
        name: predix-zone-id
        description: Cloud Foundry service instance id
      responses:
        200:
          description: Successful response
      tags:
      - Retrieve
      - Current
      - Certificate