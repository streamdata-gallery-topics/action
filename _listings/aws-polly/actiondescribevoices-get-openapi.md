---
swagger: "2.0"
x-collection-name: AWS Polly
x-complete: 0
info:
  title: AWS Polly API Describe Voices
  version: 1.0.0
  description: Returns the list of voices that are available for use when requesting
    speech synthesis.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteLexicon:
    get:
      summary: Delete Lexicon
      description: Deletes the specified pronunciation lexicon stored in an AWS Region.
      operationId: deleteLexicon
      x-api-path-slug: actiondeletelexicon-get
      parameters:
      - in: query
        name: Name
        description: The name of the lexicon to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Lexicons
  /?Action=DescribeVoices:
    get:
      summary: Describe Voices
      description: Returns the list of voices that are available for use when requesting
        speech synthesis.
      operationId: describeVoices
      x-api-path-slug: actiondescribevoices-get
      parameters:
      - in: query
        name: LanguageCode
        description: The language identification tag (ISO 639 code for the language
          name-ISO 3166 country code)       for filtering the list of voices returned
        type: string
      - in: query
        name: NextToken
        description: An opaque pagination token returned from the previous     DescribeVoices
          operation
        type: string
      responses:
        200:
          description: OK
      tags:
      - voices
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