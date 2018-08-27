---
swagger: "2.0"
x-collection-name: AWS Identity and Access Management
x-complete: 0
info:
  title: AWS Identity and Access Management API Upload Server Certificate
  version: 1.0.0
  description: Uploads a server certificate entity for the AWS account.
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
  /?Action=ListServerCertificates:
    get:
      summary: List Server Certificates
      description: Lists the server certificates stored in IAM that have the specified
        path prefix.
      operationId: listServerCertificates
      x-api-path-slug: actionlistservercertificates-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: PathPrefix
        description: The path prefix for filtering the results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Serve rCertificates
  /?Action=ListSigningCertificates:
    get:
      summary: List Signing Certificates
      description: |-
        Returns information about the signing certificates associated with the specified IAM
              user.
      operationId: listSigningCertificates
      x-api-path-slug: actionlistsigningcertificates-get
      parameters:
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      - in: query
        name: UserName
        description: The name of the IAM user whose signing certificates you want
          to examine
        type: string
      responses:
        200:
          description: OK
      tags:
      - Signing Certificates
  /?Action=UpdateServerCertificate:
    get:
      summary: Update Server Certificate
      description: |-
        Updates the name and/or the path of the specified server certificate stored in
              IAM.
      operationId: updateServerCertificate
      x-api-path-slug: actionupdateservercertificate-get
      parameters:
      - in: query
        name: NewPath
        description: The new path for the server certificate
        type: string
      - in: query
        name: NewServerCertificateName
        description: The new name for the server certificate
        type: string
      - in: query
        name: ServerCertificateName
        description: The name of the server certificate that you want to update
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Certificates
  /?Action=UpdateSigningCertificate:
    get:
      summary: Update Signing Certificate
      description: |-
        Changes the status of the specified user signing certificate from active to disabled,
              or vice versa.
      operationId: updateSigningCertificate
      x-api-path-slug: actionupdatesigningcertificate-get
      parameters:
      - in: query
        name: CertificateId
        description: The ID of the signing certificate you want to update
        type: string
      - in: query
        name: Status
        description: The status you want to assign to the certificate
        type: string
      - in: query
        name: UserName
        description: The name of the IAM user the signing certificate belongs to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Signing Certificates
  /?Action=UploadServerCertificate:
    get:
      summary: Upload Server Certificate
      description: Uploads a server certificate entity for the AWS account.
      operationId: uploadServerCertificate
      x-api-path-slug: actionuploadservercertificate-get
      parameters:
      - in: query
        name: CertificateBody
        description: The contents of the public key certificate in PEM-encoded format
        type: string
      - in: query
        name: CertificateChain
        description: The contents of the certificate chain
        type: string
      - in: query
        name: Path
        description: The path for the server certificate
        type: string
      - in: query
        name: PrivateKey
        description: The contents of the private key in PEM-encoded format
        type: string
      - in: query
        name: ServerCertificateName
        description: The name for the server certificate
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