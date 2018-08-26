---
swagger: "2.0"
x-collection-name: AWS Redshift
x-complete: 1
info:
  title: AWS Redshift API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateHsmClientCertificate:
    get:
      summary: Create Hsm Client Certificate
      description: |-
        Creates an HSM client certificate that an Amazon Redshift cluster will use to connect to
                    the client's HSM in order to store and retrieve the keys used to encrypt the cluster
                    databases.
      operationId: createHsmClientCertificate
      x-api-path-slug: actioncreatehsmclientcertificate-get
      parameters:
      - in: query
        name: HsmClientCertificateIdentifier
        description: The identifier to be assigned to the new HSM client certificate
          that the cluster            will use to connect to the HSM to use the database
          encryption keys
        type: string
      - in: query
        name: Tags.Tag.N
        description: A list of tag instances
        type: string
      responses:
        200:
          description: OK
      tags:
      - HSM Client Certificates
  /?Action=DeleteHsmClientCertificate:
    get:
      summary: Delete Hsm Client Certificate
      description: Deletes the specified HSM client certificate.
      operationId: deleteHsmClientCertificate
      x-api-path-slug: actiondeletehsmclientcertificate-get
      parameters:
      - in: query
        name: HsmClientCertificateIdentifier
        description: The identifier of the HSM client certificate to be deleted
        type: string
      responses:
        200:
          description: OK
      tags:
      - HSM Client Certificates
  /?Action=DescribeHsmClientCertificates:
    get:
      summary: Describe Hsm Client Certificates
      description: Returns information about the specified HSM client certificate.
      operationId: describeHsmClientCertificates
      x-api-path-slug: actiondescribehsmclientcertificates-get
      parameters:
      - in: query
        name: HsmClientCertificateIdentifier
        description: The identifier of a specific HSM client certificate for which
          you want information
        type: string
      - in: query
        name: Marker
        description: An optional parameter that specifies the starting point to return
          a set of response            records
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of response records to return in each call
        type: string
      - in: query
        name: TagKeys.TagKey.N
        description: A tag key or keys for which you want to return all matching HSM
          client certificates            that are associated with the specified key
          or keys
        type: string
      - in: query
        name: TagValues.TagValue.N
        description: A tag value or values for which you want to return all matching
          HSM client            certificates that are associated with the specified
          tag value or values
        type: string
      responses:
        200:
          description: OK
      tags:
      - HSM Client Certificates
---