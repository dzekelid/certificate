---
swagger: "2.0"
x-collection-name: Google OAuth2
x-complete: 0
info:
  title: Google OAuth2 APIs Get Certificate
  description: Get the certification for this session.
  contact:
    name: Google
    url: https://google.com
  version: v2
host: www.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /oauth2/v2/certs:
    get:
      summary: Get Certificate
      description: Get the certification for this session.
      operationId: oauth2.getCertForOpenIdConnect
      x-api-path-slug: oauth2v2certs-get
      responses:
        200:
          description: OK
      tags:
      - Certificate
      - Certfication
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