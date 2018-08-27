swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 1
info:
  title: AWS RDS API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeCertificates:
    get:
      summary: Describe Certificates
      description: Lists the set of CA certificates provided by Amazon RDS for this
        AWS account.
      operationId: describecertificates
      x-api-path-slug: actiondescribecertificates-get
      parameters:
      - in: query
        name: CertificateIdentifier
        description: The user-supplied certificate identifier
        type: string
      - in: query
        name: Filters.Filter.N
        description: This parameter is not currently supported
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous        DescribeCertificates
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificates