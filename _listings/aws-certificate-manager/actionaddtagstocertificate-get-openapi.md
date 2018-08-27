---
swagger: "2.0"
x-collection-name: AWS Certificate Manager
x-complete: 0
info:
  title: AWS Certificate Manager API Add Tags To Certificate
  version: 1.0.0
  description: Adds one or more tags to an ACM Certificate.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddTagsToCertificate:
    get:
      summary: Add Tags To Certificate
      description: Adds one or more tags to an ACM Certificate.
      operationId: AddTagsToCertificate
      x-api-path-slug: actionaddtagstocertificate-get
      parameters:
      - in: query
        name: CertificateArn
        description: String that contains the ARN of the ACM Certificate to which
          the tag is to be applied
        type: string
      - in: query
        name: Tags
        description: The key-value pair that defines the tag
        type: string
      responses:
        200:
          description: OK
      tags:
      - Certificate Tags
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