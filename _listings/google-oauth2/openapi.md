swagger: "2.0"
x-collection-name: Google OAuth2
x-complete: 1
info:
  title: Google OAuth2
  description: obtains-enduser-authorization-grants-for-use-with-other-google-apis-
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