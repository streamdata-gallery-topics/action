---
swagger: "2.0"
x-collection-name: AWS Snowball
x-complete: 0
info:
  title: AWS Snowball API Cancel Job
  version: 1.0.0
  description: Cancels the specified job.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CancelCluster:
    get:
      summary: Cancel Cluster
      description: Cancels a cluster job.
      operationId: cancelCluster
      x-api-path-slug: actioncancelcluster-get
      parameters:
      - in: query
        name: ClusterId
        description: The 39-character ID for the cluster that you want to cancel,
          for example        CID123e4567-e89b-12d3-a456-426655440000
        type: string
      responses:
        200:
          description: OK
      tags:
      - Clusters
  /?Action=CancelJob:
    get:
      summary: Cancel Job
      description: Cancels the specified job.
      operationId: cancelJob
      x-api-path-slug: actioncanceljob-get
      parameters:
      - in: query
        name: JobId
        description: The 39-character job ID for the job that you want to cancel,
          for example        JID123e4567-e89b-12d3-a456-426655440000
        type: string
      responses:
        200:
          description: OK
      tags:
      - Jobs
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