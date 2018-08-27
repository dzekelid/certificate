swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost
  version: 1.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /saml/certificate/idp:
    post:
      summary: Upload IDP certificate
      description: |-
        Upload the IDP certificate to be used with your SAML configuration. This will also set the filename for the IdpCertificateFile setting in your `config.json`.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: upload-the-idp-certificate-to-be-used-with-your-saml-configuration-this-will-also-set-the-filename-f
      x-api-path-slug: samlcertificateidp-post
      parameters:
      - in: formData
        name: certificate
        description: The IDP certificate file
      responses:
        200:
          description: OK
      tags:
      - Upload
      - IDP
      - Certificate
    delete:
      summary: Remove IDP certificate
      description: |-
        Delete the current IDP certificate being used with your SAML configuration. This will also disable SAML on your system as this certificate is required for SAML.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: delete-the-current-idp-certificate-being-used-with-your-saml-configuration-this-will-also-disable-sa
      x-api-path-slug: samlcertificateidp-delete
      responses:
        200:
          description: OK
      tags:
      - Remove
      - IDP
      - Certificate
  /saml/certificate/public:
    post:
      summary: Upload public certificate
      description: |-
        Upload the public certificate to be used for encryption with your SAML configuration. This will also set the filename for the PublicCertificateFile setting in your `config.json`.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: upload-the-public-certificate-to-be-used-for-encryption-with-your-saml-configuration-this-will-also-
      x-api-path-slug: samlcertificatepublic-post
      parameters:
      - in: formData
        name: certificate
        description: The public certificate file
      responses:
        200:
          description: OK
      tags:
      - Upload
      - Public
      - Certificate
    delete:
      summary: Remove public certificate
      description: |-
        Delete the current public certificate being used with your SAML configuration. This will also disable encryption for SAML on your system as this certificate is required for that.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: delete-the-current-public-certificate-being-used-with-your-saml-configuration-this-will-also-disable
      x-api-path-slug: samlcertificatepublic-delete
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Public
      - Certificate
  /saml/certificate/status:
    get:
      summary: Get certificate status
      description: |-
        Get the status of the uploaded certificates and keys in use by your SAML configuration.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: get-the-status-of-the-uploaded-certificates-and-keys-in-use-by-your-saml-configuration-permissionsmu
      x-api-path-slug: samlcertificatestatus-get
      responses:
        200:
          description: OK
      tags:
      - Certificate
      - Status