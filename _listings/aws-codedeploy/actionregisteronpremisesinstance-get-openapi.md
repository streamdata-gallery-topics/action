---
swagger: "2.0"
x-collection-name: AWS CodeDeploy
x-complete: 0
info:
  title: AWS CodeDeploy API Register On Premises Instance
  version: 1.0.0
  description: Registers an on-premises instance.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddTagsToOnPremisesInstances:
    get:
      summary: Add Tags To On Premises Instances
      description: Adds tags to on-premises instances.
      operationId: addTagsToOnPremisesInstances
      x-api-path-slug: actionaddtagstoonpremisesinstances-get
      parameters:
      - in: query
        name: instanceNames
        description: The names of the on-premises instances to which to add tags
        type: string
      - in: query
        name: tags
        description: The tag key-value pairs to add to the on-premises instances
        type: string
      responses:
        200:
          description: OK
      tags:
      - Premises Instances Tags
  /?Action=BatchGetApplicationRevisions:
    get:
      summary: Batch Get Application Revisions
      description: Gets information about one or more application revisions.
      operationId: batchGetApplicationRevisions
      x-api-path-slug: actionbatchgetapplicationrevisions-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application about which to get
          revision            information
        type: string
      - in: query
        name: revisions
        description: Information to get about the application revisions, including
          type and            location
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=BatchGetApplications:
    get:
      summary: Batch Get Applications
      description: Gets information about one or more applications.
      operationId: batchGetApplications
      x-api-path-slug: actionbatchgetapplications-get
      parameters:
      - in: query
        name: applicationNames
        description: A list of application names separated by spaces
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=BatchGetDeploymentGroups:
    get:
      summary: Batch Get Deployment Groups
      description: Gets information about one or more deployment groups.
      operationId: batchGetDeploymentGroups
      x-api-path-slug: actionbatchgetdeploymentgroups-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: deploymentGroupNames
        description: The deployment groups names
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Groups
  /?Action=BatchGetDeploymentInstances:
    get:
      summary: Batch Get Deployment Instances
      description: |-
        Gets information about one or more instance that are part of a deployment
                    group.
      operationId: batchGetDeploymentInstances
      x-api-path-slug: actionbatchgetdeploymentinstances-get
      parameters:
      - in: query
        name: deploymentId
        description: The unique ID of a deployment
        type: string
      - in: query
        name: instanceIds
        description: The unique IDs of instances in the deployment group
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Instances
  /?Action=BatchGetDeployments:
    get:
      summary: Batch Get Deployments
      description: Gets information about one or more deployments.
      operationId: batchGetDeployments
      x-api-path-slug: actionbatchgetdeployments-get
      parameters:
      - in: query
        name: deploymentIds
        description: A list of deployment IDs, separated by spaces
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=BatchGetOnPremisesInstances:
    get:
      summary: Batch Get On Premises Instances
      description: Gets information about one or more on-premises instances.
      operationId: batchGetOnPremisesInstances
      x-api-path-slug: actionbatchgetonpremisesinstances-get
      parameters:
      - in: query
        name: instanceNames
        description: The names of the on-premises instances about which to get information
        type: string
      responses:
        200:
          description: OK
      tags:
      - On Premises Instances
  /?Action=CreateApplication:
    get:
      summary: Create Application
      description: Creates an application.
      operationId: createApplication
      x-api-path-slug: actioncreateapplication-get
      parameters:
      - in: query
        name: applicationName
        description: The name of the application
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=CreateDeployment:
    get:
      summary: Create Deployment
      description: Deploys an application revision through the specified deployment
        group.
      operationId: createDeployment
      x-api-path-slug: actioncreatedeployment-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: autoRollbackConfiguration
        description: Configuration information for an automatic rollback that is added
          when a deployment            is created
        type: string
      - in: query
        name: deploymentConfigName
        description: The name of a deployment configuration associated with the applicable
          IAM user or            AWS account
        type: string
      - in: query
        name: deploymentGroupName
        description: The name of the deployment group
        type: string
      - in: query
        name: description
        description: A comment about the deployment
        type: string
      - in: query
        name: ignoreApplicationStopFailures
        description: If set to true, then if the deployment causes the ApplicationStop
          deployment            lifecycle event to an instance to fail, the deployment
          to that instance will not be            considered to have failed at that
          point and will continue on to the BeforeInstall            deployment lifecycle
          event
        type: string
      - in: query
        name: revision
        description: The type and location of the revision to deploy
        type: string
      - in: query
        name: updateOutdatedInstancesOnly
        description: Indicates whether to deploy to all instances or only to instances
          that are not            running the latest application revision
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=CreateDeploymentConfig:
    get:
      summary: Create Deployment Config
      description: Creates a deployment configuration.
      operationId: createDeploymentConfig
      x-api-path-slug: actioncreatedeploymentconfig-get
      parameters:
      - in: query
        name: deploymentConfigName
        description: The name of the deployment configuration to create
        type: string
      - in: query
        name: minimumHealthyHosts
        description: The minimum number of healthy instances that should be available
          at any time during            the deployment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=CreateDeploymentGroup:
    get:
      summary: Create Deployment Group
      description: |-
        Creates a deployment group to which application revisions will be
                    deployed.
      operationId: createDeploymentGroup
      x-api-path-slug: actioncreatedeploymentgroup-get
      parameters:
      - in: query
        name: alarmConfiguration
        description: Information to add about Amazon CloudWatch alarms when the deployment
          group is            created
        type: string
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: autoRollbackConfiguration
        description: Configuration information for an automatic rollback that is added
          when a deployment            group is created
        type: string
      - in: query
        name: autoScalingGroups
        description: A list of associated Auto Scaling groups
        type: string
      - in: query
        name: deploymentConfigName
        description: If specified, the deployment configuration name can be either
          one of the predefined            configurations provided with AWS CodeDeploy
          or a custom deployment configuration that            you create by calling
          the create deployment configuration operation
        type: string
      - in: query
        name: deploymentGroupName
        description: The name of a new deployment group for the specified application
        type: string
      - in: query
        name: ec2TagFilters
        description: The Amazon EC2 tags on which to filter
        type: string
      - in: query
        name: onPremisesInstanceTagFilters
        description: The on-premises instance tags on which to filter
        type: string
      - in: query
        name: serviceRoleArn
        description: A service role ARN that allows AWS CodeDeploy to act on the users
          behalf when            interacting with AWS services
        type: string
      - in: query
        name: triggerConfigurations
        description: Information about triggers to create when the deployment group
          is created
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Groups
  /?Action=DeleteApplication:
    get:
      summary: Delete Application
      description: Deletes an application.
      operationId: deleteApplication
      x-api-path-slug: actiondeleteapplication-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=DeleteDeploymentConfig:
    get:
      summary: Delete Deployment Config
      description: Deletes a deployment configuration.
      operationId: deleteDeploymentConfig
      x-api-path-slug: actiondeletedeploymentconfig-get
      parameters:
      - in: query
        name: deploymentConfigName
        description: The name of a deployment configuration associated with the applicable
          IAM user or            AWS account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=DeleteDeploymentGroup:
    get:
      summary: Delete Deployment Group
      description: Deletes a deployment group.
      operationId: deleteDeploymentGroup
      x-api-path-slug: actiondeletedeploymentgroup-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: deploymentGroupName
        description: The name of an existing deployment group for the specified application
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Groups
  /?Action=DeregisterOnPremisesInstance:
    get:
      summary: Deregister On Premises Instance
      description: Deregisters an on-premises instance.
      operationId: deregisterOnPremisesInstance
      x-api-path-slug: actionderegisteronpremisesinstance-get
      parameters:
      - in: query
        name: instanceName
        description: The name of the on-premises instance to deregister
        type: string
      responses:
        200:
          description: OK
      tags:
      - On Premises Instances
  /?Action=GetApplication:
    get:
      summary: Get Application
      description: Gets information about an application.
      operationId: getApplication
      x-api-path-slug: actiongetapplication-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=GetApplicationRevision:
    get:
      summary: Get Application Revision
      description: Gets information about an application revision.
      operationId: getApplicationRevision
      x-api-path-slug: actiongetapplicationrevision-get
      parameters:
      - in: query
        name: applicationName
        description: The name of the application that corresponds to the revision
        type: string
      - in: query
        name: revision
        description: Information about the application revision to get, including
          type and            location
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=GetDeployment:
    get:
      summary: Get Deployment
      description: Gets information about a deployment.
      operationId: getDeployment
      x-api-path-slug: actiongetdeployment-get
      parameters:
      - in: query
        name: deploymentId
        description: A deployment ID associated with the applicable IAM user or AWS
          account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=GetDeploymentConfig:
    get:
      summary: Get Deployment Config
      description: Gets information about a deployment configuration.
      operationId: getDeploymentConfig
      x-api-path-slug: actiongetdeploymentconfig-get
      parameters:
      - in: query
        name: deploymentConfigName
        description: The name of a deployment configuration associated with the applicable
          IAM user or            AWS account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=GetDeploymentGroup:
    get:
      summary: Get Deployment Group
      description: Gets information about a deployment group.
      operationId: getDeploymentGroup
      x-api-path-slug: actiongetdeploymentgroup-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: deploymentGroupName
        description: The name of an existing deployment group for the specified application
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Groups
  /?Action=GetDeploymentInstance:
    get:
      summary: Get Deployment Instance
      description: Gets information about an instance as part of a deployment.
      operationId: getDeploymentInstance
      x-api-path-slug: actiongetdeploymentinstance-get
      parameters:
      - in: query
        name: deploymentId
        description: The unique ID of a deployment
        type: string
      - in: query
        name: instanceId
        description: The unique ID of an instance in the deployment group
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Instances
  /?Action=GetOnPremisesInstance:
    get:
      summary: Get On Premises Instance
      description: Gets information about an on-premises instance.
      operationId: getOnPremisesInstance
      x-api-path-slug: actiongetonpremisesinstance-get
      parameters:
      - in: query
        name: instanceName
        description: The name of the on-premises instance about which to get information
        type: string
      responses:
        200:
          description: OK
      tags:
      - On Premises Instances
  /?Action=ListApplicationRevisions:
    get:
      summary: List Application Revisions
      description: Lists information about revisions for an application.
      operationId: listApplicationRevisions
      x-api-path-slug: actionlistapplicationrevisions-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: deployed
        description: 'Whether to list revisions based on whether the revision is the
          target revision of            an deployment group:'
        type: string
      - in: query
        name: nextToken
        description: An identifier returned from the previous list application revisions
          call
        type: string
      - in: query
        name: s3Bucket
        description: An Amazon S3 bucket name to limit the search for revisions
        type: string
      - in: query
        name: s3KeyPrefix
        description: A key prefix for the set of Amazon S3 objects to limit the search
          for            revisions
        type: string
      - in: query
        name: sortBy
        description: 'The column name to use to sort the list results:'
        type: string
      - in: query
        name: sortOrder
        description: 'The order in which to sort the list results:'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=ListApplications:
    get:
      summary: List Applications
      description: |-
        Lists the applications registered with the applicable IAM user or AWS
                    account.
      operationId: listApplications
      x-api-path-slug: actionlistapplications-get
      parameters:
      - in: query
        name: nextToken
        description: An identifier returned from the previous list applications call
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=ListDeploymentConfigs:
    get:
      summary: List Deployment Configs
      description: |-
        Lists the deployment configurations with the applicable IAM user or AWS
                    account.
      operationId: listDeploymentConfigs
      x-api-path-slug: actionlistdeploymentconfigs-get
      parameters:
      - in: query
        name: nextToken
        description: An identifier returned from the previous list deployment configurations
          call
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=ListDeploymentGroups:
    get:
      summary: List Deployment Groups
      description: |-
        Lists the deployment groups for an application registered with the applicable IAM
                    user or AWS account.
      operationId: listDeploymentGroups
      x-api-path-slug: actionlistdeploymentgroups-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: nextToken
        description: An identifier returned from the previous list deployment groups
          call
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Groups
  /?Action=ListDeploymentInstances:
    get:
      summary: List Deployment Instances
      description: |-
        Lists the instance for a deployment associated with the applicable IAM user or AWS
                    account.
      operationId: listDeploymentInstances
      x-api-path-slug: actionlistdeploymentinstances-get
      parameters:
      - in: query
        name: deploymentId
        description: The unique ID of a deployment
        type: string
      - in: query
        name: instanceStatusFilter
        description: 'A subset of instances to list by status:'
        type: string
      - in: query
        name: nextToken
        description: An identifier returned from the previous list deployment instances
          call
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployment Instances
  /?Action=ListDeployments:
    get:
      summary: List Deployments
      description: |-
        Lists the deployments in a deployment group for an application registered with the
                    applicable IAM user or AWS account.
      operationId: listDeployments
      x-api-path-slug: actionlistdeployments-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: createTimeRange
        description: A time range (start and end) for returning a subset of the list
          of            deployments
        type: string
      - in: query
        name: deploymentGroupName
        description: The name of an existing deployment group for the specified application
        type: string
      - in: query
        name: includeOnlyStatuses
        description: 'A subset of deployments to list by status:'
        type: string
      - in: query
        name: nextToken
        description: An identifier returned from the previous list deployments call
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deployments
  /?Action=ListOnPremisesInstances:
    get:
      summary: List On Premises Instances
      description: Gets a list of names for one or more on-premises instances.
      operationId: listOnPremisesInstances
      x-api-path-slug: actionlistonpremisesinstances-get
      parameters:
      - in: query
        name: nextToken
        description: An identifier returned from the previous list on-premises instances
          call
        type: string
      - in: query
        name: registrationStatus
        description: 'The registration status of the on-premises instances:'
        type: string
      - in: query
        name: tagFilters
        description: The on-premises instance tags that will be used to restrict the
          corresponding            on-premises instance names returned
        type: string
      responses:
        200:
          description: OK
      tags:
      - On Premises Instances
  /?Action=RegisterApplicationRevision:
    get:
      summary: Register Application Revision
      description: Registers with AWS CodeDeploy a revision for the specified application.
      operationId: registerApplicationRevision
      x-api-path-slug: actionregisterapplicationrevision-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: description
        description: A comment about the revision
        type: string
      - in: query
        name: revision
        description: Information about the application revision to register, including
          type and            location
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=RegisterOnPremisesInstance:
    get:
      summary: Register On Premises Instance
      description: Registers an on-premises instance.
      operationId: registerOnPremisesInstance
      x-api-path-slug: actionregisteronpremisesinstance-get
      parameters:
      - in: query
        name: iamSessionArn
        description: The ARN of the IAM session to associate with the on-premises
          instance
        type: string
      - in: query
        name: iamUserArn
        description: The ARN of the IAM user to associate with the on-premises instance
        type: string
      - in: query
        name: instanceName
        description: The name of the on-premises instance to register
        type: string
      responses:
        200:
          description: OK
      tags:
      - On Premises Instances
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