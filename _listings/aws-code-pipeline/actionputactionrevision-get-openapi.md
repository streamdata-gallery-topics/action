---
swagger: "2.0"
x-collection-name: AWS Code Pipeline
x-complete: 0
info:
  title: AWS Code Pipeline API Put Action Revision
  version: 1.0.0
  description: Provides information to AWS CodePipeline about new revisions to a source.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateCustomActionType:
    get:
      summary: Create Custom Action Type
      description: |-
        Creates a new custom action that can be used in all pipelines associated with the
                    AWS account.
      operationId: createCustomActionType
      x-api-path-slug: actioncreatecustomactiontype-get
      parameters:
      - in: query
        name: Attribute
        description: The snapshot attribute you would like to view
        type: string
      - in: query
        name: category
        description: The category of the custom action, such as a build action or
          a test            action
        type: string
      - in: query
        name: configurationProperties
        description: The configuration properties for the custom action
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: inputArtifactDetails
        description: Returns information about the details of an artifact
        type: string
      - in: query
        name: outputArtifactDetails
        description: Returns information about the details of an artifact
        type: string
      - in: query
        name: provider
        description: The provider of the service used in the custom action, such as
          AWS            CodeDeploy
        type: string
      - in: query
        name: settings
        description: Returns information about the settings for an action type
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the EBS snapshot
        type: string
      - in: query
        name: version
        description: The version identifier of the custom action
        type: string
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Action
      - Type
  /?Action=DeleteCustomActionType:
    get:
      summary: Delete Custom Action Type
      description: Marks a custom action as deleted.
      operationId: deleteCustomActionType
      x-api-path-slug: actiondeletecustomactiontype-get
      parameters:
      - in: query
        name: Attribute
        description: The instance attribute
        type: string
      - in: query
        name: category
        description: The category of the custom action that you want to delete, such
          as source or            deploy
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: provider
        description: The provider of the service used in the custom action, such as
          AWS            CodeDeploy
        type: string
      - in: query
        name: version
        description: The version of the custom action to delete
        type: string
      - in: query
        name: VolumeId
        description: The ID of the volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Action
      - Type
  /?Action=ListActionTypes:
    get:
      summary: List Action Types
      description: |-
        Gets a summary of all AWS CodePipeline action types associated with your
                    account.
      operationId: listActionTypes
      x-api-path-slug: actionlistactiontypes-get
      parameters:
      - in: query
        name: actionOwnerFilter
        description: Filters the list of action types to those created by a specified
          entity
        type: string
      - in: query
        name: AllocationId
        description: '[EC2-VPC] The allocation ID'
        type: string
      - in: query
        name: AllowReassociation
        description: '[EC2-VPC] For a VPC in an EC2-Classic account, specify true
          to allow an Elastic IP address that is already associated with an instance
          or network interface to be reassociated with the specified instance or network
          interface'
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: NetworkInterfaceId
        description: '[EC2-VPC] The ID of the network interface'
        type: string
      - in: query
        name: nextToken
        description: An identifier that was returned from the previous list action
          types call, which can            be used to return the next set of action
          types in the list
        type: string
      - in: query
        name: PrivateIpAddress
        description: '[EC2-VPC] The primary or secondary private IP address to associate
          with the Elastic IP address'
        type: string
      - in: query
        name: PublicIp
        description: The Elastic IP address
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Action
      - Types
  /?Action=PutActionRevision:
    get:
      summary: Put Action Revision
      description: Provides information to AWS CodePipeline about new revisions to
        a source.
      operationId: putActionRevision
      x-api-path-slug: actionputactionrevision-get
      parameters:
      - in: query
        name: actionName
        description: The name of the action that will process the revision
        type: string
      - in: query
        name: actionRevision
        description: Represents information about the version (or revision) of an
          action
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: pipelineName
        description: The name of the pipeline that will start processing the revision
          to the            source
        type: string
      - in: query
        name: PublicIp
        description: The Elastic IP address
        type: string
      - in: query
        name: stageName
        description: The name of the stage that contains the action that will act
          upon the            revision
        type: string
      responses:
        200:
          description: OK
      tags:
      - Put
      - Action
      - Revision
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