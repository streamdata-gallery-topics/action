---
swagger: "2.0"
x-collection-name: LoginRadius
x-complete: 0
info:
  title: Matrix Login Operations API Submit a login action.
  version: 1.0.0
  description: If this is part of a multi-stage login, there MUST be a session key.
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: /login
basePath: http://localhost:8008/_matrix/client/api/v1
paths:
  /login:
    post:
      summary: Submit a login action.
      description: If this is part of a multi-stage login, there MUST be a session
        key.
      operationId: submit_login
      x-api-path-slug: login-post
      parameters:
      - in: body
        name: body
        description: A login submission
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Submit
      - Login
      - Action
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