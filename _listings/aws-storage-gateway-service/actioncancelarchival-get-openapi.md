---
swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 0
info:
  title: AWS Storage Gateway Service API Cancel Archival
  version: 1.0.0
  description: |-
    Cancels archiving of a virtual tape to the virtual tape shelf (VTS) after the
             archiving process is initiated.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ActivateGateway:
    get:
      summary: Activate Gateway
      description: Activates the gateway you previously deployed on your host.
      operationId: activateGateway
      x-api-path-slug: actionactivategateway-get
      parameters:
      - in: query
        name: ActivationKey
        description: Your gateway activation key
        type: string
      - in: query
        name: GatewayName
        description: The name you configured for your gateway
        type: string
      - in: query
        name: GatewayRegion
        description: A value that indicates the region where you want to store the
          snapshot backups
        type: string
      - in: query
        name: GatewayTimezone
        description: A value that indicates the time zone you want to set for the
          gateway
        type: string
      - in: query
        name: GatewayType
        description: A value that defines the type of gateway to activate
        type: string
      - in: query
        name: MediumChangerType
        description: The value that indicates the type of medium changer to use for
          gateway-VTL
        type: string
      - in: query
        name: TapeDriveType
        description: The value that indicates the type of tape drive to use for gateway-VTL
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gateway
  /?Action=AddCache:
    get:
      summary: Add Cache
      description: Configures one or more gateway local disks as cache for a cached-volume
        gateway.
      operationId: addCache
      x-api-path-slug: actionaddcache-get
      parameters:
      - in: query
        name: DiskIds
        description: 'Type: array of Strings'
        type: string
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache
  /?Action=AddTagsToResource:
    get:
      summary: Add Tags To Resource
      description: Adds one or more tags to the specified resource.
      operationId: addTagsToResource
      x-api-path-slug: actionaddtagstoresource-get
      parameters:
      - in: query
        name: ResourceARN
        description: The Amazon Resource Name (ARN) of the resource you want to add
          tags to
        type: string
      - in: query
        name: Tags
        description: The key-value pair that represents the tag you want to add to
          the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tags
  /?Action=AddUploadBuffer:
    get:
      summary: Add Upload Buffer
      description: Configures one or more gateway local disks as upload buffer for
        a specified gateway.
      operationId: addUploadBuffer
      x-api-path-slug: actionadduploadbuffer-get
      parameters:
      - in: query
        name: DiskIds
        description: 'Type: array of Strings'
        type: string
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Upload Buffer
  /?Action=AddWorkingStorage:
    get:
      summary: Add Working Storage
      description: Configures one or more gateway local disks as working storage for
        a gateway.
      operationId: addWorkingStorage
      x-api-path-slug: actionaddworkingstorage-get
      parameters:
      - in: query
        name: DiskIds
        description: An array of strings that identify disks that are to be configured
          as working storage
        type: string
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      responses:
        200:
          description: OK
      tags:
      - Working Storage
  /?Action=CancelArchival:
    get:
      summary: Cancel Archival
      description: |-
        Cancels archiving of a virtual tape to the virtual tape shelf (VTS) after the
                 archiving process is initiated.
      operationId: cancelArchival
      x-api-path-slug: actioncancelarchival-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: TapeARN
        description: The Amazon Resource Name (ARN) of the virtual tape you want to
          cancel archiving         for
        type: string
      responses:
        200:
          description: OK
      tags:
      - Archival
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