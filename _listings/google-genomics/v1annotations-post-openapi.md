---
swagger: "2.0"
x-collection-name: Google Genomics
x-complete: 0
info:
  title: Google Genomics API Create Annotation
  description: |-
    Creates a new annotation. Caller must have WRITE permission
    for the associated annotation set.

    The following fields are required:

    * annotationSetId
    * referenceName or
      referenceId

    ### Transcripts

    For annotations of type TRANSCRIPT, the following fields of
    transcript must be provided:

    * exons.start
    * exons.end

    All other fields may be optionally specified, unless documented as being
    server-generated (for example, the `id` field). The annotated
    range must be no longer than 100Mbp (mega base pairs). See the
    Annotation resource
    for additional restrictions on each field.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: genomics.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/annotations:
    post:
      summary: Create Annotation
      description: |-
        Creates a new annotation. Caller must have WRITE permission
        for the associated annotation set.

        The following fields are required:

        * annotationSetId
        * referenceName or
          referenceId

        ### Transcripts

        For annotations of type TRANSCRIPT, the following fields of
        transcript must be provided:

        * exons.start
        * exons.end

        All other fields may be optionally specified, unless documented as being
        server-generated (for example, the `id` field). The annotated
        range must be no longer than 100Mbp (mega base pairs). See the
        Annotation resource
        for additional restrictions on each field.
      operationId: genomics.annotations.create
      x-api-path-slug: v1annotations-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Annotation
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