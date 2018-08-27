---
swagger: "2.0"
x-collection-name: AWS Internet of Things
x-complete: 0
info:
  title: AWS Internet of Things API List Certificates
  version: 1.0.0
  description: Lists the certificates registered in your AWS account.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AcceptCertificateTransfer:
    get:
      summary: Accept Certificate Transfer
      description: Accepts a pending certificate transfer.
      operationId: acceptCertificateTransfer
      x-api-path-slug: actionacceptcertificatetransfer-get
      parameters:
      - in: query
        name: certificateId
        description: The ID of the certificate
        type: string
      - in: query
        name: setAsActive
        description: Specifies whether the certificate is active
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificate Transfers
  /?Action=CancelCertificateTransfer:
    get:
      summary: Cancel Certificate Transfer
      description: Cancels a pending transfer for the specified certificate.
      operationId: cancelCertificateTransfer
      x-api-path-slug: actioncancelcertificatetransfer-get
      parameters:
      - in: query
        name: certificateId
        description: The ID of the certificate
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificate Transfers
  /?Action=CreateCertificateFromCsr:
    get:
      summary: Create Certificate From Csr
      description: Creates an X.
      operationId: createCertificateFromCsr
      x-api-path-slug: actioncreatecertificatefromcsr-get
      parameters:
      - in: query
        name: certificateSigningRequest
        description: The certificate signing request (CSR)
        type: string
      - in: query
        name: setAsActive
        description: Specifies whether the certificate is active
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificates
  /?Action=CreateKeysAndCertificate:
    get:
      summary: Create Keys And Certificate
      description: Creates a 2048-bit RSA key pair and issues an X.
      operationId: createKeysAndCertificate
      x-api-path-slug: actioncreatekeysandcertificate-get
      parameters:
      - in: query
        name: setAsActive
        description: Specifies whether the certificate is active
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys And Certificates
  /?Action=DeleteCACertificate:
    get:
      summary: Delete C A Certificate
      description: Deletes a registered CA certificate.
      operationId: deleteCACertificate
      x-api-path-slug: actiondeletecacertificate-get
      parameters:
      - in: query
        name: certificateId
        description: The ID of the certificate to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - CA Certificates
  /?Action=DeleteCertificate:
    get:
      summary: Delete Certificate
      description: Deletes the specified certificate.
      operationId: deleteCertificate
      x-api-path-slug: actiondeletecertificate-get
      parameters:
      - in: query
        name: certificateId
        description: The ID of the certificate
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificates
  /?Action=DescribeCACertificate:
    get:
      summary: Describe C A Certificate
      description: Describes a registered CA certificate.
      operationId: describeCACertificate
      x-api-path-slug: actiondescribecacertificate-get
      parameters:
      - in: query
        name: certificateId
        description: The CA certificate identifier
        type: string
      responses:
        200:
          description: OK
      tags:
      - CA Certificates
  /?Action=DescribeCertificate:
    get:
      summary: Describe Certificate
      description: Gets information about the specified certificate.
      operationId: describeCertificate
      x-api-path-slug: actiondescribecertificate-get
      parameters:
      - in: query
        name: certificateId
        description: The ID of the certificate
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificates
  /?Action=ListCACertificates:
    get:
      summary: List C A Certificates
      description: Lists the CA certificates registered for your AWS account.
      operationId: listCACertificates
      x-api-path-slug: actionlistcacertificates-get
      parameters:
      - in: query
        name: ascendingOrder
        description: Determines the order of the results
        type: string
      - in: query
        name: marker
        description: The marker for the next set of results
        type: string
      - in: query
        name: pageSize
        description: The result page size
        type: string
      responses:
        200:
          description: OK
      tags:
      - CA Certificates
  /?Action=ListCertificates:
    get:
      summary: List Certificates
      description: Lists the certificates registered in your AWS account.
      operationId: listCertificates
      x-api-path-slug: actionlistcertificates-get
      parameters:
      - in: query
        name: ascendingOrder
        description: Specifies the order for results
        type: string
      - in: query
        name: marker
        description: The marker for the next set of results
        type: string
      - in: query
        name: pageSize
        description: The result page size
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificates
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