---
swagger: "2.0"
x-collection-name: AWS Identity and Access Management
x-complete: 0
info:
  title: AWS Identity and Access Management API Get Server Certificate
  version: 1.0.0
  description: Retrieves information about the specified server certificate stored
    in IAM.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteServerCertificate:
    get:
      summary: Delete Server Certificate
      description: Deletes the specified server certificate.
      operationId: deleteServerCertificate
      x-api-path-slug: actiondeleteservercertificate-get
      parameters:
      - in: query
        name: ServerCertificateName
        description: The name of the server certificate you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Certificates
  /?Action=DeleteSigningCertificate:
    get:
      summary: Delete Signing Certificate
      description: Deletes a signing certificate associated with the specified IAM
        user.
      operationId: deleteSigningCertificate
      x-api-path-slug: actiondeletesigningcertificate-get
      parameters:
      - in: query
        name: CertificateId
        description: The ID of the signing certificate to delete
        type: string
      - in: query
        name: UserName
        description: The name of the user the signing certificate belongs to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Signing Certificates
  /?Action=GetServerCertificate:
    get:
      summary: Get Server Certificate
      description: Retrieves information about the specified server certificate stored
        in IAM.
      operationId: getServerCertificate
      x-api-path-slug: actiongetservercertificate-get
      parameters:
      - in: query
        name: ServerCertificateName
        description: The name of the server certificate you want to retrieve information
          about
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Certificates
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