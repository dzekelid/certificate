---
swagger: "2.0"
x-collection-name: DigitalOcean
x-complete: 0
info:
  title: Digital Ocean Retrieve an existing certificate
  description: "To show information about an existing certificate, send a GET request
    to /v2/certificates/$CERTIFICATE_ID.\r\n\r\nThe response will be a JSON object
    with a certificate key."
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /certificates:
    post:
      summary: Create a new certificate
      description: To upload or create a new SSL certificate, send a POST request
        to /v2/certificates. When uploading a user-generated certificate, the private_key,
        leaf_certificate, and optionally the certificate_chain attributes should be
        provided. The type should be set to "custom". When generating a certificate
        using Let's Encrypt, the dns_names attribute must be provided, and the type
        should be set to "lets_encrypt".
      operationId: CertificatesPost
      x-api-path-slug: certificates-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - New
      - Certificate
  /certificates/892071a0-bb95-49bc-8021-3afd67a210bf:
    get:
      summary: Retrieve an existing certificate
      description: "To show information about an existing certificate, send a GET
        request to /v2/certificates/$CERTIFICATE_ID.\r\n\r\nThe response will be a
        JSON object with a certificate key."
      operationId: Certificates892071a0Bb9549bc80213afd67a210bfGet
      x-api-path-slug: certificates892071a0bb9549bc80213afd67a210bf-get
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Existing
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