swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
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