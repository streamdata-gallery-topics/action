---
swagger: "2.0"
x-collection-name: AWS Key Management Service
x-complete: 0
info:
  title: AWS Key Management Service API Generate Random
  version: 1.0.0
  description: Generates an unpredictable byte string.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CancelKeyDeletion:
    get:
      summary: Cancel Key Deletion
      description: Cancels the deletion of a customer master key (CMK).
      operationId: cancelKeyDeletion
      x-api-path-slug: actioncancelkeydeletion-get
      parameters:
      - in: query
        name: KeyId
        description: The unique identifier for the customer master key (CMK) for which
          to cancel      deletion
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=CreateAlias:
    get:
      summary: Create Alias
      description: Creates a display name for a customer master key.
      operationId: createAlias
      x-api-path-slug: actioncreatealias-get
      parameters:
      - in: query
        name: AliasName
        description: String that contains the display name
        type: string
      - in: query
        name: TargetKeyId
        description: An identifier of the key for which you are creating the alias
        type: string
      responses:
        200:
          description: OK
      tags:
      - Aliases
  /?Action=CreateGrant:
    get:
      summary: Create Grant
      description: Adds a grant to a key to specify who can use the key and under
        what conditions.
      operationId: createGrant
      x-api-path-slug: actioncreategrant-get
      parameters:
      - in: query
        name: Constraints
        description: The conditions under which the operations permitted by the grant
          are allowed
        type: string
      - in: query
        name: GranteePrincipal
        description: The principal that is given permission to perform the operations
          that the grant      permits
        type: string
      - in: query
        name: GrantTokens
        description: A list of grant tokens
        type: string
      - in: query
        name: KeyId
        description: The unique identifier for the customer master key (CMK) that
          the grant applies      to
        type: string
      - in: query
        name: Name
        description: A friendly name for identifying the grant
        type: string
      - in: query
        name: Operations
        description: A list of operations that the grant permits
        type: string
      - in: query
        name: RetiringPrincipal
        description: The principal that is given permission to retire the grant by
          using RetireGrant operation
        type: string
      responses:
        200:
          description: OK
      tags:
      - Grants
  /?Action=CreateKey:
    get:
      summary: Create Key
      description: Creates a customer master key (CMK).
      operationId: createKey
      x-api-path-slug: actioncreatekey-get
      parameters:
      - in: query
        name: BypassPolicyLockoutSafetyCheck
        description: A flag to indicate whether to bypass the key policy lockout safety
          check
        type: string
      - in: query
        name: Description
        description: A description of the CMK
        type: string
      - in: query
        name: KeyUsage
        description: The intended use of the CMK
        type: string
      - in: query
        name: Origin
        description: The source of the CMKs key material
        type: string
      - in: query
        name: Policy
        description: The key policy to attach to the CMK
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=Decrypt:
    get:
      summary: Decrypt
      description: Decrypts ciphertext.
      operationId: decrypt
      x-api-path-slug: actiondecrypt-get
      parameters:
      - in: query
        name: CiphertextBlob
        description: Ciphertext to be decrypted
        type: string
      - in: query
        name: EncryptionContext
        description: The encryption context
        type: string
      - in: query
        name: GrantTokens
        description: A list of grant tokens
        type: string
      responses:
        200:
          description: OK
      tags:
      - Decrypt
  /?Action=DeleteAlias:
    get:
      summary: Delete Alias
      description: Deletes the specified alias.
      operationId: deleteAlias
      x-api-path-slug: actiondeletealias-get
      parameters:
      - in: query
        name: AliasName
        description: The alias to be deleted
        type: string
      responses:
        200:
          description: OK
      tags:
      - Aliases
  /?Action=DeleteImportedKeyMaterial:
    get:
      summary: Delete Imported Key Material
      description: |-
        Deletes key material that you previously imported and makes the specified customer
              master key (CMK) unusable.
      operationId: deleteImportedKeyMaterial
      x-api-path-slug: actiondeleteimportedkeymaterial-get
      parameters:
      - in: query
        name: KeyId
        description: The identifier of the CMK whose key material to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=DescribeKey:
    get:
      summary: Describe Key
      description: Provides detailed information about the specified customer master
        key.
      operationId: describeKey
      x-api-path-slug: actiondescribekey-get
      parameters:
      - in: query
        name: GrantTokens
        description: A list of grant tokens
        type: string
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=DisableKey:
    get:
      summary: Disable Key
      description: |-
        Sets the state of a customer master key (CMK) to disabled, thereby preventing its use
              for cryptographic operations.
      operationId: disableKey
      x-api-path-slug: actiondisablekey-get
      parameters:
      - in: query
        name: KeyId
        description: A unique identifier for the CMK
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=DisableKeyRotation:
    get:
      summary: Disable Key Rotation
      description: Disables rotation of the specified key.
      operationId: disableKeyRotation
      x-api-path-slug: actiondisablekeyrotation-get
      parameters:
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=EnableKey:
    get:
      summary: Enable Key
      description: Marks a key as enabled, thereby permitting its use.
      operationId: enableKey
      x-api-path-slug: actionenablekey-get
      parameters:
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=EnableKeyRotation:
    get:
      summary: Enable Key Rotation
      description: Enables rotation of the specified customer master key.
      operationId: enableKeyRotation
      x-api-path-slug: actionenablekeyrotation-get
      parameters:
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=Encrypt:
    get:
      summary: Encrypt
      description: Encrypts plaintext into ciphertext by using a customer master key.
      operationId: encrypt
      x-api-path-slug: actionencrypt-get
      parameters:
      - in: query
        name: EncryptionContext
        description: Name-value pair that specifies the encryption context to be used
          for authenticated      encryption
        type: string
      - in: query
        name: GrantTokens
        description: A list of grant tokens
        type: string
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key
        type: string
      - in: query
        name: Plaintext
        description: Data to be encrypted
        type: string
      responses:
        200:
          description: OK
      tags:
      - Encrypt
  /?Action=GenerateDataKey:
    get:
      summary: Generate Data Key
      description: |-
        Returns a data encryption key that you can use in your application to encrypt
              data locally.
      operationId: generateDataKey
      x-api-path-slug: actiongeneratedatakey-get
      parameters:
      - in: query
        name: EncryptionContext
        description: A set of key-value pairs that represents additional authenticated
          data
        type: string
      - in: query
        name: GrantTokens
        description: A list of grant tokens
        type: string
      - in: query
        name: KeyId
        description: The identifier of the CMK under which to generate and encrypt
          the data encryption      key
        type: string
      - in: query
        name: KeySpec
        description: The length of the data encryption key
        type: string
      - in: query
        name: NumberOfBytes
        description: The length of the data encryption key in bytes
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=GenerateDataKeyWithoutPlaintext:
    get:
      summary: Generate Data Key Without Plaintext
      description: Returns a data encryption key encrypted under a customer master
        key (CMK).
      operationId: generateDataKeyWithoutPlaintext
      x-api-path-slug: actiongeneratedatakeywithoutplaintext-get
      parameters:
      - in: query
        name: EncryptionContext
        description: A set of key-value pairs that represents additional authenticated
          data
        type: string
      - in: query
        name: GrantTokens
        description: A list of grant tokens
        type: string
      - in: query
        name: KeyId
        description: The identifier of the CMK under which to generate and encrypt
          the data encryption      key
        type: string
      - in: query
        name: KeySpec
        description: The length of the data encryption key
        type: string
      - in: query
        name: NumberOfBytes
        description: The length of the data encryption key in bytes
        type: string
      responses:
        200:
          description: OK
      tags:
      - Keys
  /?Action=GenerateRandom:
    get:
      summary: Generate Random
      description: Generates an unpredictable byte string.
      operationId: generateRandom
      x-api-path-slug: actiongeneraterandom-get
      parameters:
      - in: query
        name: NumberOfBytes
        description: The length of the byte string
        type: string
      responses:
        200:
          description: OK
      tags:
      - Randoms
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