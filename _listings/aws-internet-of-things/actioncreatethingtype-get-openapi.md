---
swagger: "2.0"
x-collection-name: AWS Internet of Things
x-complete: 0
info:
  title: AWS Internet of Things API Create Thing Type
  version: 1.0.0
  description: Creates a new thing type.
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
  /?Action=AttachPrincipalPolicy:
    get:
      summary: Attach Principal Policy
      description: Attaches the specified policy to the specified principal (certificate
        or other credential).
      operationId: attachPrincipalPolicy
      x-api-path-slug: actionattachprincipalpolicy-get
      parameters:
      - in: query
        name: policyName
        description: The policy name
        type: string
      - in: query
        name: principal
        description: The principal, which can be a certificate ARN (as returned from
          the CreateCertificate operation) or an Amazon Cognito ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Principal Policies
  /?Action=AttachThingPrincipal:
    get:
      summary: Attach Thing Principal
      description: Attaches the specified principal to the specified thing.
      operationId: attachThingPrincipal
      x-api-path-slug: actionattachthingprincipal-get
      parameters:
      - in: query
        name: principal
        description: The principal, such as a certificate or other credential
        type: string
      - in: query
        name: thingName
        description: The name of the thing
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Principals
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
  /?Action=CreatePolicy:
    get:
      summary: Create Policy
      description: Creates an AWS IoT policy.
      operationId: createPolicy
      x-api-path-slug: actioncreatepolicy-get
      parameters:
      - in: query
        name: policyDocument
        description: The JSON document that describes the policy
        type: string
      - in: query
        name: policyName
        description: The policy name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=CreatePolicyVersion:
    get:
      summary: Create Policy Version
      description: Creates a new version of the specified AWS IoT policy.
      operationId: createPolicyVersion
      x-api-path-slug: actioncreatepolicyversion-get
      parameters:
      - in: query
        name: policyDocument
        description: The JSON document that describes the policy
        type: string
      - in: query
        name: policyName
        description: The policy name
        type: string
      - in: query
        name: setAsDefault
        description: Specifies whether the policy version is set as the default
        type: string
      responses:
        200:
          description: OK
      tags:
      - Policies
  /?Action=CreateThing:
    get:
      summary: Create Thing
      description: Creates a thing record in the thing registry.
      operationId: createThing
      x-api-path-slug: actioncreatething-get
      parameters:
      - in: query
        name: attributePayload
        description: The attribute payload, which consists of up to three name/value
          pairs in a JSON document
        type: string
      - in: query
        name: thingName
        description: The name of the thing to create
        type: string
      - in: query
        name: thingTypeName
        description: The name of the thing type associated with the new thing
        type: string
      responses:
        200:
          description: OK
      tags:
      - Things
  /?Action=CreateThingType:
    get:
      summary: Create Thing Type
      description: Creates a new thing type.
      operationId: createThingType
      x-api-path-slug: actioncreatethingtype-get
      parameters:
      - in: query
        name: thingTypeName
        description: The name of the thing type
        type: string
      - in: query
        name: thingTypeProperties
        description: The ThingTypeProperties for the thing type to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Thing Types
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