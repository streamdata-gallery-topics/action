---
swagger: "2.0"
x-collection-name: AWS Direct Connect
x-complete: 0
info:
  title: AWS Direct Connect API Allocate Connection On Interconnect
  version: 1.0.0
  description: Creates a hosted connection on an interconnect.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AllocateConnectionOnInterconnect:
    get:
      summary: Allocate Connection On Interconnect
      description: Creates a hosted connection on an interconnect.
      operationId: allocateConnectionOnInterconnect
      x-api-path-slug: actionallocateconnectiononinterconnect-get
      parameters:
      - in: query
        name: bandwidth
        description: Bandwidth of the connection
        type: string
      - in: query
        name: connectionName
        description: Name of the provisioned connection
        type: string
      - in: query
        name: interconnectId
        description: ID of the interconnect on which the connection will be provisioned
        type: string
      - in: query
        name: ownerAccount
        description: Numeric account Id of the customer for whom the connection will
          be provisioned
        type: string
      - in: query
        name: vlan
        description: The dedicated VLAN provisioned to the connection
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
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