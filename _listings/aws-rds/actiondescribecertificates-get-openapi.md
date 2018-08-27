---
swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 0
info:
  title: Amazon RDS API Describe Certificates
  version: 1.0.0
  description: Lists the set of CA certificates provided by Amazon RDS for this AWS
    account.
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