---
swagger: "2.0"
x-collection-name: Google Genomics
x-complete: 0
info:
  title: Google Genomics API Create Batch Annotation
  description: |-
    Creates one or more new annotations atomically. All annotations must
    belong to the same annotation set. Caller must have WRITE
    permission for this annotation set. For optimal performance, batch
    positionally adjacent annotations together.

    If the request has a systemic issue, such as an attempt to write to
    an inaccessible annotation set, the entire RPC will fail accordingly. For
    lesser data issues, when possible an error will be isolated to the
    corresponding batch entry in the response; the remaining well formed
    annotations will be created normally.

    For details on the requirements for each individual annotation resource,
    see
    CreateAnnotation.
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
  /v1/annotations/search:
    post:
      summary: Search Annotations
      description: |-
        Searches for annotations that match the given criteria. Results are
        ordered by genomic coordinate (by reference sequence, then position).
        Annotations with equivalent genomic coordinates are returned in an
        unspecified order. This order is consistent, such that two queries for the
        same content (regardless of page size) yield annotations in the same order
        across their respective streams of paginated responses. Caller must have
        READ permission for the queried annotation sets.
      operationId: genomics.annotations.search
      x-api-path-slug: v1annotationssearch-post
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
  /v1/annotations/{annotationId}:
    delete:
      summary: Delete Annotation
      description: |-
        Deletes an annotation. Caller must have WRITE permission for
        the associated annotation set.
      operationId: genomics.annotations.delete
      x-api-path-slug: v1annotationsannotationid-delete
      parameters:
      - in: path
        name: annotationId
        description: The ID of the annotation to be deleted
      responses:
        200:
          description: OK
      tags:
      - Annotation
    get:
      summary: Get Annotation
      description: |-
        Gets an annotation. Caller must have READ permission
        for the associated annotation set.
      operationId: genomics.annotations.get
      x-api-path-slug: v1annotationsannotationid-get
      parameters:
      - in: path
        name: annotationId
        description: The ID of the annotation to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Annotation
    put:
      summary: Update Annotation
      description: |-
        Updates an annotation. Caller must have
        WRITE permission for the associated dataset.
      operationId: genomics.annotations.update
      x-api-path-slug: v1annotationsannotationid-put
      parameters:
      - in: path
        name: annotationId
        description: The ID of the annotation to be updated
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: updateMask
        description: An optional mask specifying which fields to update
      responses:
        200:
          description: OK
      tags:
      - Annotation
  /v1/annotations:batchCreate:
    post:
      summary: Create Batch Annotation
      description: |-
        Creates one or more new annotations atomically. All annotations must
        belong to the same annotation set. Caller must have WRITE
        permission for this annotation set. For optimal performance, batch
        positionally adjacent annotations together.

        If the request has a systemic issue, such as an attempt to write to
        an inaccessible annotation set, the entire RPC will fail accordingly. For
        lesser data issues, when possible an error will be isolated to the
        corresponding batch entry in the response; the remaining well formed
        annotations will be created normally.

        For details on the requirements for each individual annotation resource,
        see
        CreateAnnotation.
      operationId: genomics.annotations.batchCreate
      x-api-path-slug: v1annotationsbatchcreate-post
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