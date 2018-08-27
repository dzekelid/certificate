---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 0
info:
  title: Google Compute Engine API Get SSL Certificate
  description: Returns the specified SslCertificate resource. Get a list of available
    SSL certificates by making a list() request.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/global/sslCertificates:
    get:
      summary: Get SSL Certificates
      description: Retrieves the list of SslCertificate resources available to the
        specified project.
      operationId: compute.sslCertificates.list
      x-api-path-slug: projectglobalsslcertificates-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Certificate
    post:
      summary: Create SSL Certificate
      description: Creates a SslCertificate resource in the specified project using
        the data included in the request.
      operationId: compute.sslCertificates.insert
      x-api-path-slug: projectglobalsslcertificates-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Certificate
  /{project}/global/sslCertificates/{sslCertificate}:
    delete:
      summary: Delete SSL Certificate
      description: Deletes the specified SslCertificate resource.
      operationId: compute.sslCertificates.delete
      x-api-path-slug: projectglobalsslcertificatessslcertificate-delete
      parameters:
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: sslCertificate
        description: Name of the SslCertificate resource to delete
      responses:
        200:
          description: OK
      tags:
      - Certificate
    get:
      summary: Get SSL Certificate
      description: Returns the specified SslCertificate resource. Get a list of available
        SSL certificates by making a list() request.
      operationId: compute.sslCertificates.get
      x-api-path-slug: projectglobalsslcertificatessslcertificate-get
      parameters:
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: sslCertificate
        description: Name of the SslCertificate resource to return
      responses:
        200:
          description: OK
      tags:
      - Certificate
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