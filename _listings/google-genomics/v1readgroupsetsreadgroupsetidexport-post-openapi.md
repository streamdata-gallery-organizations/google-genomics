---
swagger: "2.0"
x-collection-name: Google Genomics
x-complete: 0
info:
  title: Google Genomics API Export Read Group Set
  description: |-
    Exports a read group set to a BAM file in Google Cloud Storage.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Note that currently there may be some differences between exported BAM
    files and the original BAM file at the time of import. See
    ImportReadGroupSets
    for caveats.
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
  /v1/annotationsets:
    post:
      summary: Create Annotation Set
      description: |-
        Creates a new annotation set. Caller must have WRITE permission for the
        associated dataset.

        The following fields are required:

          * datasetId
          * referenceSetId

        All other fields may be optionally specified, unless documented as being
        server-generated (for example, the `id` field).
      operationId: genomics.annotationsets.create
      x-api-path-slug: v1annotationsets-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Annotation Set
  /v1/annotationsets/search:
    post:
      summary: Search Annotation Sets
      description: |-
        Searches for annotation sets that match the given criteria. Annotation sets
        are returned in an unspecified order. This order is consistent, such that
        two queries for the same content (regardless of page size) yield annotation
        sets in the same order across their respective streams of paginated
        responses. Caller must have READ permission for the queried datasets.
      operationId: genomics.annotationsets.search
      x-api-path-slug: v1annotationsetssearch-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Annotation Set
  /v1/annotationsets/{annotationSetId}:
    delete:
      summary: Delete Annotation Set
      description: |-
        Deletes an annotation set. Caller must have WRITE permission
        for the associated annotation set.
      operationId: genomics.annotationsets.delete
      x-api-path-slug: v1annotationsetsannotationsetid-delete
      parameters:
      - in: path
        name: annotationSetId
        description: The ID of the annotation set to be deleted
      responses:
        200:
          description: OK
      tags:
      - Annotation Set
    get:
      summary: Get Annotation Set
      description: |-
        Gets an annotation set. Caller must have READ permission for
        the associated dataset.
      operationId: genomics.annotationsets.get
      x-api-path-slug: v1annotationsetsannotationsetid-get
      parameters:
      - in: path
        name: annotationSetId
        description: The ID of the annotation set to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Annotation Set
    put:
      summary: Update Annotation Set
      description: |-
        Updates an annotation set. The update must respect all mutability
        restrictions and other invariants described on the annotation set resource.
        Caller must have WRITE permission for the associated dataset.
      operationId: genomics.annotationsets.update
      x-api-path-slug: v1annotationsetsannotationsetid-put
      parameters:
      - in: path
        name: annotationSetId
        description: The ID of the annotation set to be updated
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
      - Annotation Set
  /v1/callsets:
    post:
      summary: Create Call Set
      description: |-
        Creates a new call set.

        For the definitions of call sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.callsets.create
      x-api-path-slug: v1callsets-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Call Set
  /v1/callsets/search:
    post:
      summary: Search Call Sets
      description: |-
        Gets a list of call sets matching the criteria.

        For the definitions of call sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        Implements
        [GlobalAllianceApi.searchCallSets](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/variantmethods.avdl#L178).
      operationId: genomics.callsets.search
      x-api-path-slug: v1callsetssearch-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Call Set
  /v1/callsets/{callSetId}:
    delete:
      summary: Delete Call Set
      description: |-
        Deletes a call set.

        For the definitions of call sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.callsets.delete
      x-api-path-slug: v1callsetscallsetid-delete
      parameters:
      - in: path
        name: callSetId
        description: The ID of the call set to be deleted
      responses:
        200:
          description: OK
      tags:
      - Call Set
    get:
      summary: Get Call Set
      description: |-
        Gets a call set by ID.

        For the definitions of call sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.callsets.get
      x-api-path-slug: v1callsetscallsetid-get
      parameters:
      - in: path
        name: callSetId
        description: The ID of the call set
      responses:
        200:
          description: OK
      tags:
      - Call Set
    patch:
      summary: Update Call Set
      description: |-
        Updates a call set.

        For the definitions of call sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        This method supports patch semantics.
      operationId: genomics.callsets.patch
      x-api-path-slug: v1callsetscallsetid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: callSetId
        description: The ID of the call set to be updated
      - in: query
        name: updateMask
        description: An optional mask specifying which fields to update
      responses:
        200:
          description: OK
      tags:
      - Call Set
  /v1/datasets:
    get:
      summary: Get Datasets
      description: |-
        Lists datasets within a project.

        For the definitions of datasets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.datasets.list
      x-api-path-slug: v1datasets-get
      parameters:
      - in: query
        name: pageSize
        description: The maximum number of results to return in a single page
      - in: query
        name: pageToken
        description: The continuation token, which is used to page through large result
          sets
      - in: query
        name: projectId
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Dataset
    post:
      summary: Create Dataset
      description: |-
        Creates a new dataset.

        For the definitions of datasets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.datasets.create
      x-api-path-slug: v1datasets-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dataset
  /v1/datasets/{datasetId}:
    delete:
      summary: Delete Dataset
      description: |-
        Deletes a dataset and all of its contents (all read group sets,
        reference sets, variant sets, call sets, annotation sets, etc.)
        This is reversible (up to one week after the deletion) via
        the
        datasets.undelete
        operation.

        For the definitions of datasets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.datasets.delete
      x-api-path-slug: v1datasetsdatasetid-delete
      parameters:
      - in: path
        name: datasetId
        description: The ID of the dataset to be deleted
      responses:
        200:
          description: OK
      tags:
      - Dataset
    get:
      summary: Get Dataset
      description: |-
        Gets a dataset by ID.

        For the definitions of datasets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.datasets.get
      x-api-path-slug: v1datasetsdatasetid-get
      parameters:
      - in: path
        name: datasetId
        description: The ID of the dataset
      responses:
        200:
          description: OK
      tags:
      - Dataset
    patch:
      summary: Update Dataset
      description: |-
        Updates a dataset.

        For the definitions of datasets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        This method supports patch semantics.
      operationId: genomics.datasets.patch
      x-api-path-slug: v1datasetsdatasetid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: datasetId
        description: The ID of the dataset to be updated
      - in: query
        name: updateMask
        description: An optional mask specifying which fields to update
      responses:
        200:
          description: OK
      tags:
      - Dataset
  /v1/datasets/{datasetId}:undelete:
    post:
      summary: Restore Dataset
      description: |-
        Undeletes a dataset by restoring a dataset which was deleted via this API.

        For the definitions of datasets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        This operation is only possible for a week after the deletion occurred.
      operationId: genomics.datasets.undelete
      x-api-path-slug: v1datasetsdatasetidundelete-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: datasetId
        description: The ID of the dataset to be undeleted
      responses:
        200:
          description: OK
      tags:
      - Dataset
  /v1/readgroupsets/search:
    post:
      summary: Search Read Group Sets
      description: |-
        Searches for read group sets matching the criteria.

        For the definitions of read group sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        Implements
        [GlobalAllianceApi.searchReadGroupSets](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/readmethods.avdl#L135).
      operationId: genomics.readgroupsets.search
      x-api-path-slug: v1readgroupsetssearch-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Read Group Set
  /v1/readgroupsets/{readGroupSetId}:
    delete:
      summary: Delete Read Group Set
      description: |-
        Deletes a read group set.

        For the definitions of read group sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.readgroupsets.delete
      x-api-path-slug: v1readgroupsetsreadgroupsetid-delete
      parameters:
      - in: path
        name: readGroupSetId
        description: The ID of the read group set to be deleted
      responses:
        200:
          description: OK
      tags:
      - Read Group Set
    get:
      summary: Get Read Group Set
      description: |-
        Gets a read group set by ID.

        For the definitions of read group sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
      operationId: genomics.readgroupsets.get
      x-api-path-slug: v1readgroupsetsreadgroupsetid-get
      parameters:
      - in: path
        name: readGroupSetId
        description: The ID of the read group set
      responses:
        200:
          description: OK
      tags:
      - Read Group Set
    patch:
      summary: Update Read Group Set
      description: |-
        Updates a read group set.

        For the definitions of read group sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        This method supports patch semantics.
      operationId: genomics.readgroupsets.patch
      x-api-path-slug: v1readgroupsetsreadgroupsetid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: readGroupSetId
        description: The ID of the read group set to be updated
      - in: query
        name: updateMask
        description: An optional mask specifying which fields to update
      responses:
        200:
          description: OK
      tags:
      - Read Group Set
  /v1/readgroupsets/{readGroupSetId}/coveragebuckets:
    get:
      summary: Get Coverage Buckets for Read Group Set
      description: |-
        Lists fixed width coverage buckets for a read group set, each of which
        correspond to a range of a reference sequence. Each bucket summarizes
        coverage information across its corresponding genomic range.

        For the definitions of read group sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        Coverage is defined as the number of reads which are aligned to a given
        base in the reference sequence. Coverage buckets are available at several
        precomputed bucket widths, enabling retrieval of various coverage 'zoom
        levels'. The caller must have READ permissions for the target read group
        set.
      operationId: genomics.readgroupsets.coveragebuckets.list
      x-api-path-slug: v1readgroupsetsreadgroupsetidcoveragebuckets-get
      parameters:
      - in: query
        name: end
        description: The end position of the range on the reference, 0-based exclusive
      - in: query
        name: pageSize
        description: The maximum number of results to return in a single page
      - in: query
        name: pageToken
        description: The continuation token, which is used to page through large result
          sets
      - in: path
        name: readGroupSetId
        description: Required
      - in: query
        name: referenceName
        description: The name of the reference to query, within the reference set
          associatedwith this query
      - in: query
        name: start
        description: The start position of the range on the reference, 0-based inclusive
      - in: query
        name: targetBucketWidth
        description: The desired width of each reported coverage bucket in base pairs
      responses:
        200:
          description: OK
      tags:
      - Read Group Set
  /v1/readgroupsets/{readGroupSetId}:export:
    post:
      summary: Export Read Group Set
      description: |-
        Exports a read group set to a BAM file in Google Cloud Storage.

        For the definitions of read group sets and other genomics resources, see
        [Fundamentals of Google
        Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

        Note that currently there may be some differences between exported BAM
        files and the original BAM file at the time of import. See
        ImportReadGroupSets
        for caveats.
      operationId: genomics.readgroupsets.export
      x-api-path-slug: v1readgroupsetsreadgroupsetidexport-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: readGroupSetId
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Read Group Set
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