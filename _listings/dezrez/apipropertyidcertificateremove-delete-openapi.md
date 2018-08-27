---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Remove certificate from a property
  version: 1.0.0
  description: Remove certificate from a property.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/property/{id}/certificate/remove:
    delete:
      summary: Remove certificate from a property
      description: Remove certificate from a property.
      operationId: Property_RemoveCertificateByidBycertificateId
      x-api-path-slug: apipropertyidcertificateremove-delete
      parameters:
      - in: query
        name: certificateId
        description: The ids of the certificate to remove
      - in: path
        name: id
        description: The property id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Certificate
      - From
      - Property
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