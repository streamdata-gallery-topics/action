---
swagger: "2.0"
x-collection-name: Azure Blockchain Workbench
x-complete: 0
info:
  title: Azure Blockchain Workbench Post Contracts Actions
  description: |-
    Executes an action for the specified smart contract instance and action ID. Users are only able to execute
                 the action given the current state of the specified smart contract instance and the user's associated application role
                 or smart contract instance role.
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/contracts/{contractId}/actions:
    get:
      summary: Get Contracts Actions
      description: |-
        Lists all actions, which can be taken by the given user and current state of the specified smart contract
                     instance. Users get all applicable actions if the user has an associated application role or is associated with a smart
                     contract instance role for the current state of the specified smart contract instance.
      operationId: ContractActionsGet
      x-api-path-slug: apiv1contractscontractidactions-get
      parameters:
      - in: path
        name: contractId
        description: The id of the contract
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
      - Contracts
      - Actions
    post:
      summary: Post Contracts Actions
      description: |-
        Executes an action for the specified smart contract instance and action ID. Users are only able to execute
                     the action given the current state of the specified smart contract instance and the user's associated application role
                     or smart contract instance role.
      operationId: ContractActionPost
      x-api-path-slug: apiv1contractscontractidactions-post
      parameters:
      - in: body
        name: actionInformation
        description: Parameters for a particular action
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: contractId
        description: The id of the contract
      responses:
        200:
          description: OK
      tags:
      - Contracts
      - Actions
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