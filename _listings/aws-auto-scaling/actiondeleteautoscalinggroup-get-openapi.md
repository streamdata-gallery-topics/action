---
swagger: "2.0"
x-collection-name: AWS Auto Scaling
x-complete: 0
info:
  title: AWS Auto Scaling API Delete Auto Scaling Group
  version: 1.0.0
  description: Deletes the specified Auto Scaling group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AttachInstances:
    get:
      summary: Attach Instances
      description: Attaches one or more EC2 instances to the specified Auto Scaling
        group.
      operationId: attachInstances
      x-api-path-slug: actionattachinstances-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: InstanceIds.member.N
        description: One or more instance IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=AttachLoadBalancers:
    get:
      summary: Attach Load Balancers
      description: Attaches one or more Classic load balancers to the specified Auto
        Scaling group.
      operationId: attachLoadBalancers
      x-api-path-slug: actionattachloadbalancers-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: LoadBalancerNames.member.N
        description: One or more load balancer names
        type: string
      responses:
        200:
          description: OK
      tags:
      - Load Balancers
  /?Action=AttachLoadBalancerTargetGroups:
    get:
      summary: Attach Load Balancer Target Groups
      description: Attaches one or more target groups to the specified Auto Scaling
        group.
      operationId: attachLoadBalancerTargetGroups
      x-api-path-slug: actionattachloadbalancertargetgroups-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the Auto Scaling group
        type: string
      - in: query
        name: TargetGroupARNs.member.N
        description: The Amazon Resource Names (ARN) of the target groups
        type: string
      responses:
        200:
          description: OK
      tags:
      - Load Balancers
  /?Action=CompleteLifecycleAction:
    get:
      summary: Complete Lifecycle Action
      description: Completes the lifecycle action for the specified token or instance
        with the specified result.
      operationId: completeLifecycleAction
      x-api-path-slug: actioncompletelifecycleaction-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group for the lifecycle hook
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: LifecycleActionResult
        description: The action for the group to take
        type: string
      - in: query
        name: LifecycleActionToken
        description: A universally unique identifier (UUID) that identifies a specific
          lifecycle action associated with an instance
        type: string
      - in: query
        name: LifecycleHookName
        description: The name of the lifecycle hook
        type: string
      responses:
        200:
          description: OK
      tags:
      - Life Cycle
  /?Action=CreateAutoScalingGroup:
    get:
      summary: Create Auto Scaling Group
      description: Creates an Auto Scaling group with the specified name and attributes.
      operationId: createAutoScalingGroup
      x-api-path-slug: actioncreateautoscalinggroup-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: AvailabilityZones.member.N
        description: One or more Availability Zones for the group
        type: string
      - in: query
        name: DefaultCooldown
        description: The amount of time, in seconds, after a scaling activity completes
          before another scaling activity can start
        type: string
      - in: query
        name: DesiredCapacity
        description: The number of EC2 instances that should be running in the group
        type: string
      - in: query
        name: HealthCheckGracePeriod
        description: The amount of time, in seconds, that Auto Scaling waits before
          checking the health status of an EC2 instance that has come into service
        type: string
      - in: query
        name: HealthCheckType
        description: The service to use for the health checks
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance used to create a launch configuration
          for the group
        type: string
      - in: query
        name: LaunchConfigurationName
        description: The name of the launch configuration
        type: string
      - in: query
        name: LoadBalancerNames.member.N
        description: One or more Classic load balancers
        type: string
      - in: query
        name: MaxSize
        description: The maximum size of the group
        type: string
      - in: query
        name: MinSize
        description: The minimum size of the group
        type: string
      - in: query
        name: NewInstancesProtectedFromScaleIn
        description: Indicates whether newly launched instances are protected from
          termination by Auto Scaling when scaling in
        type: string
      - in: query
        name: PlacementGroup
        description: The name of the placement group into which youll launch your
          instances, if any
        type: string
      - in: query
        name: Tags.member.N
        description: One or more tags
        type: string
      - in: query
        name: TargetGroupARNs.member.N
        description: The Amazon Resource Names (ARN) of the target groups
        type: string
      - in: query
        name: TerminationPolicies.member.N
        description: One or more termination policies used to select the instance
          to terminate
        type: string
      - in: query
        name: VPCZoneIdentifier
        description: A comma-separated list of subnet identifiers for your virtual
          private cloud (VPC)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Auto Scaling Groups
  /?Action=CreateLaunchConfiguration:
    get:
      summary: Create Launch Configuration
      description: Creates a launch configuration.
      operationId: createLaunchConfiguration
      x-api-path-slug: actioncreatelaunchconfiguration-get
      parameters:
      - in: query
        name: AssociatePublicIpAddress
        description: Used for groups that launch instances into a virtual private
          cloud (VPC)
        type: string
      - in: query
        name: BlockDeviceMappings.member.N
        description: One or more mappings that specify how block devices are exposed
          to the instance
        type: string
      - in: query
        name: ClassicLinkVPCId
        description: The ID of a ClassicLink-enabled VPC to link your EC2-Classic
          instances to
        type: string
      - in: query
        name: ClassicLinkVPCSecurityGroups.member.N
        description: The IDs of one or more security groups for the specified ClassicLink-enabled
          VPC
        type: string
      - in: query
        name: EbsOptimized
        description: Indicates whether the instance is optimized for Amazon EBS I/O
        type: string
      - in: query
        name: IamInstanceProfile
        description: The name or the Amazon Resource Name (ARN) of the instance profile
          associated with the IAM role for the instance
        type: string
      - in: query
        name: ImageId
        description: The ID of the Amazon Machine Image (AMI) to use to launch your
          EC2 instances
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance to use to create the launch configuration
        type: string
      - in: query
        name: InstanceMonitoring
        description: Enables detailed monitoring (true) or basic monitoring (false)
          for the Auto Scaling instances
        type: string
      - in: query
        name: InstanceType
        description: The instance type of the EC2 instance
        type: string
      - in: query
        name: KernelId
        description: The ID of the kernel associated with the AMI
        type: string
      - in: query
        name: KeyName
        description: The name of the key pair
        type: string
      - in: query
        name: LaunchConfigurationName
        description: The name of the launch configuration
        type: string
      - in: query
        name: PlacementTenancy
        description: The tenancy of the instance
        type: string
      - in: query
        name: RamdiskId
        description: The ID of the RAM disk associated with the AMI
        type: string
      - in: query
        name: SecurityGroups.member.N
        description: One or more security groups with which to associate the instances
        type: string
      - in: query
        name: SpotPrice
        description: The maximum hourly price to be paid for any Spot Instance launched
          to fulfill the request
        type: string
      - in: query
        name: UserData
        description: The user data to make available to the launched EC2 instances
        type: string
      responses:
        200:
          description: OK
      tags:
      - Launch
  /?Action=CreateOrUpdateTags:
    get:
      summary: Create Or Update Tags
      description: Creates or updates tags for the specified Auto Scaling group.
      operationId: createOrUpdateTags
      x-api-path-slug: actioncreateorupdatetags-get
      parameters:
      - in: query
        name: Tags.member.N
        description: One or more tags
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tags
  /?Action=DeleteAutoScalingGroup:
    get:
      summary: Delete Auto Scaling Group
      description: Deletes the specified Auto Scaling group.
      operationId: deleteAutoScalingGroup
      x-api-path-slug: actiondeleteautoscalinggroup-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group to delete
        type: string
      - in: query
        name: ForceDelete
        description: Specifies that the group will be deleted along with all instances
          associated with the group, without waiting for all instances to be terminated
        type: string
      responses:
        200:
          description: OK
      tags:
      - Auto Scaling Groups
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