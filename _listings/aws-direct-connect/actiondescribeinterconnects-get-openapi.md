---
swagger: "2.0"
x-collection-name: AWS Direct Connect
x-complete: 0
info:
  title: AWS Direct Connect API Describe Interconnects
  version: 1.0.0
  description: Returns a list of interconnects owned by the AWS account.
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
  /?Action=AllocatePrivateVirtualInterface:
    get:
      summary: Allocate Private Virtual Interface
      description: Provisions a private virtual interface to be owned by a different
        customer.
      operationId: allocatePrivateVirtualInterface
      x-api-path-slug: actionallocateprivatevirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: The connection ID on which the private virtual interface is provisioned
        type: string
      - in: query
        name: newPrivateVirtualInterfaceAllocation
        description: Detailed information for the private virtual interface to be
          provisioned
        type: string
      - in: query
        name: ownerAccount
        description: The AWS account that will own the new private virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=AllocatePublicVirtualInterface:
    get:
      summary: Allocate Public Virtual Interface
      description: Provisions a public virtual interface to be owned by a different
        customer.
      operationId: allocatePublicVirtualInterface
      x-api-path-slug: actionallocatepublicvirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: The connection ID on which the public virtual interface is provisioned
        type: string
      - in: query
        name: newPublicVirtualInterfaceAllocation
        description: Detailed information for the public virtual interface to be provisioned
        type: string
      - in: query
        name: ownerAccount
        description: The AWS account that will own the new public virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=ConfirmConnection:
    get:
      summary: Confirm Connection
      description: Confirm the creation of a hosted connection on an interconnect.
      operationId: confirmConnection
      x-api-path-slug: actionconfirmconnection-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=ConfirmPrivateVirtualInterface:
    get:
      summary: Confirm Private Virtual Interface
      description: Accept ownership of a private virtual interface created by another
        customer.
      operationId: confirmPrivateVirtualInterface
      x-api-path-slug: actionconfirmprivatevirtualinterface-get
      parameters:
      - in: query
        name: virtualGatewayId
        description: ID of the virtual private gateway that will be attached to the
          virtual interface
        type: string
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=ConfirmPublicVirtualInterface:
    get:
      summary: Confirm Public Virtual Interface
      description: Accept ownership of a public virtual interface created by another
        customer.
      operationId: confirmPublicVirtualInterface
      x-api-path-slug: actionconfirmpublicvirtualinterface-get
      parameters:
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=CreateBGPPeer:
    get:
      summary: Create B G P Peer
      description: Creates a new BGP peer on a specified virtual interface.
      operationId: createBGPPeer
      x-api-path-slug: actioncreatebgppeer-get
      parameters:
      - in: query
        name: newBGPPeer
        description: Detailed information for the BGP peer to be created
        type: string
      - in: query
        name: virtualInterfaceId
        description: The ID of the virtual interface on which the BGP peer will be
          provisioned
        type: string
      responses:
        200:
          description: OK
      tags:
      - BGP Peer
  /?Action=CreateConnection:
    get:
      summary: Create Connection
      description: Creates a new connection between the customer network and a specific
        AWS Direct Connect location.
      operationId: createConnection
      x-api-path-slug: actioncreateconnection-get
      parameters:
      - in: query
        name: bandwidth
        description: Bandwidth of the connection
        type: string
      - in: query
        name: connectionName
        description: The name of the connection
        type: string
      - in: query
        name: location
        description: Where the connection is located
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=CreateInterconnect:
    get:
      summary: Create Interconnect
      description: Creates a new interconnect between a AWS Direct Connect partner's
        network and a specific AWS Direct Connect location.
      operationId: createInterconnect
      x-api-path-slug: actioncreateinterconnect-get
      parameters:
      - in: query
        name: bandwidth
        description: The port bandwidth
        type: string
      - in: query
        name: interconnectName
        description: The name of the interconnect
        type: string
      - in: query
        name: location
        description: Where the interconnect is located
        type: string
      responses:
        200:
          description: OK
      tags:
      - Interconnects
  /?Action=CreatePrivateVirtualInterface:
    get:
      summary: Create Private Virtual Interface
      description: Creates a new private virtual interface.
      operationId: createPrivateVirtualInterface
      x-api-path-slug: actioncreateprivatevirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: newPrivateVirtualInterface
        description: Detailed information for the private virtual interface to be
          created
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=CreatePublicVirtualInterface:
    get:
      summary: Create Public Virtual Interface
      description: Creates a new public virtual interface.
      operationId: createPublicVirtualInterface
      x-api-path-slug: actioncreatepublicvirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: newPublicVirtualInterface
        description: Detailed information for the public virtual interface to be created
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=DeleteBGPPeer:
    get:
      summary: Delete B G P Peer
      description: Deletes a BGP peer on the specified virtual interface that matches
        the specified customer address and ASN.
      operationId: deleteBGPPeer
      x-api-path-slug: actiondeletebgppeer-get
      parameters:
      - in: query
        name: asn
        description: Autonomous system (AS) number for Border Gateway Protocol (BGP)
          configuration
        type: string
      - in: query
        name: customerAddress
        description: IP address assigned to the customer interface
        type: string
      - in: query
        name: virtualInterfaceId
        description: The ID of the virtual interface from which the BGP peer will
          be deleted
        type: string
      responses:
        200:
          description: OK
      tags:
      - BGP Peer
  /?Action=DeleteConnection:
    get:
      summary: Delete Connection
      description: Deletes the connection.
      operationId: deleteConnection
      x-api-path-slug: actiondeleteconnection-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=DeleteInterconnect:
    get:
      summary: Delete Interconnect
      description: Deletes the specified interconnect.
      operationId: deleteInterconnect
      x-api-path-slug: actiondeleteinterconnect-get
      parameters:
      - in: query
        name: interconnectId
        description: The ID of the interconnect
        type: string
      responses:
        200:
          description: OK
      tags:
      - Interconnects
  /?Action=DeleteVirtualInterface:
    get:
      summary: Delete Virtual Interface
      description: Deletes a virtual interface.
      operationId: deleteVirtualInterface
      x-api-path-slug: actiondeletevirtualinterface-get
      parameters:
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Virtual Interfaces
  /?Action=DescribeConnectionLoa:
    get:
      summary: Describe Connection Loa
      description: Returns the LOA-CFA for a Connection.
      operationId: describeConnectionLoa
      x-api-path-slug: actiondescribeconnectionloa-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: loaContentType
        description: A standard media type indicating the content type of the LOA-CFA
          document
        type: string
      - in: query
        name: providerName
        description: The name of the APN partner or service provider who establishes
          connectivity on your behalf
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=DescribeConnections:
    get:
      summary: Describe Connections
      description: Displays all connections in this region.
      operationId: describeConnections
      x-api-path-slug: actiondescribeconnections-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=DescribeConnectionsOnInterconnect:
    get:
      summary: Describe Connections On Interconnect
      description: Return a list of connections that have been provisioned on the
        given interconnect.
      operationId: describeConnectionsOnInterconnect
      x-api-path-slug: actiondescribeconnectionsoninterconnect-get
      parameters:
      - in: query
        name: interconnectId
        description: ID of the interconnect on which a list of connection is provisioned
        type: string
      responses:
        200:
          description: OK
      tags:
      - Connections
  /?Action=DescribeInterconnectLoa:
    get:
      summary: Describe Interconnect Loa
      description: Returns the LOA-CFA for an Interconnect.
      operationId: describeInterconnectLoa
      x-api-path-slug: actiondescribeinterconnectloa-get
      parameters:
      - in: query
        name: interconnectId
        description: The ID of the interconnect
        type: string
      - in: query
        name: loaContentType
        description: A standard media type indicating the content type of the LOA-CFA
          document
        type: string
      - in: query
        name: providerName
        description: The name of the service provider who establishes connectivity
          on your behalf
        type: string
      responses:
        200:
          description: OK
      tags:
      - Interconnects
  /?Action=DescribeInterconnects:
    get:
      summary: Describe Interconnects
      description: Returns a list of interconnects owned by the AWS account.
      operationId: describeInterconnects
      x-api-path-slug: actiondescribeinterconnects-get
      parameters:
      - in: query
        name: interconnectId
        description: The ID of the interconnect
        type: string
      responses:
        200:
          description: OK
      tags:
      - Interconnects
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