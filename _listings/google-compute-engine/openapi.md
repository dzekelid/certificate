swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 1
info:
  title: Compute Engine
  description: creates-and-runs-virtual-machines-on-google-cloud-platform-
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
  /{project}/global/targetSslProxies/{targetSslProxy}/setSslCertificates:
    post:
      summary: Change SSL Certificate
      description: Changes SslCertificates for TargetSslProxy.
      operationId: compute.targetSslProxies.setSslCertificates
      x-api-path-slug: projectglobaltargetsslproxiestargetsslproxysetsslcertificates-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: targetSslProxy
        description: Name of the TargetSslProxy resource whose SslCertificate resource
          is to be set
      responses:
        200:
          description: OK
      tags:
      - Certificate
  /{project}/targetHttpsProxies/{targetHttpsProxy}/setSslCertificates:
    post:
      summary: Replace SSL Certificate for Target HTTP PRoxy
      description: Replaces SslCertificates for TargetHttpsProxy.
      operationId: compute.targetHttpsProxies.setSslCertificates
      x-api-path-slug: projecttargethttpsproxiestargethttpsproxysetsslcertificates-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: targetHttpsProxy
        description: Name of the TargetHttpsProxy resource to set an SslCertificates
          resource for
      responses:
        200:
          description: OK
      tags:
      - Certificate