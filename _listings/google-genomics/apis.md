---
name: Google Genomics
x-slug: google-genomics
description: Google Genomics helps the life science community organize the world&rsquo;s
  genomic information and make it accessible and useful. Big genomic data is here
  today, with petabytes rapidly growing toward exabytes. Through our extensions to
  Google Cloud Platform, you can apply the same technologies that power Google Search
  and Maps to securely store, process, explore, and share large, complex datasets.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Google Genomics
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/apis.md
specificationVersion: "0.14"
apis:
- name: Genomics - Create Annotation
  x-api-slug: v1annotations-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotations-post-openapi.md
- name: Genomics - Search Annotations
  x-api-slug: v1annotationssearch-post
  description: |-
    Searches for annotations that match the given criteria. Results are
    ordered by genomic coordinate (by reference sequence, then position).
    Annotations with equivalent genomic coordinates are returned in an
    unspecified order. This order is consistent, such that two queries for the
    same content (regardless of page size) yield annotations in the same order
    across their respective streams of paginated responses. Caller must have
    READ permission for the queried annotation sets.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationssearch-post-openapi.md
- name: Genomics - Delete Annotation
  x-api-slug: v1annotationsannotationid-delete
  description: |-
    Deletes an annotation. Caller must have WRITE permission for
    the associated annotation set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsannotationid-delete-openapi.md
- name: Genomics - Get Annotation
  x-api-slug: v1annotationsannotationid-get
  description: |-
    Gets an annotation. Caller must have READ permission
    for the associated annotation set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsannotationid-get-openapi.md
- name: Genomics - Update Annotation
  x-api-slug: v1annotationsannotationid-put
  description: |-
    Updates an annotation. Caller must have
    WRITE permission for the associated dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsannotationid-put-openapi.md
- name: Genomics - Create Batch Annotation
  x-api-slug: v1annotationsbatchcreate-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsbatchcreate-post-openapi.md
- name: Genomics - Create Annotation Set
  x-api-slug: v1annotationsets-post
  description: |-
    Creates a new annotation set. Caller must have WRITE permission for the
    associated dataset.

    The following fields are required:

      * datasetId
      * referenceSetId

    All other fields may be optionally specified, unless documented as being
    server-generated (for example, the `id` field).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsets-post-openapi.md
- name: Genomics - Search Annotation Sets
  x-api-slug: v1annotationsetssearch-post
  description: |-
    Searches for annotation sets that match the given criteria. Annotation sets
    are returned in an unspecified order. This order is consistent, such that
    two queries for the same content (regardless of page size) yield annotation
    sets in the same order across their respective streams of paginated
    responses. Caller must have READ permission for the queried datasets.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsetssearch-post-openapi.md
- name: Genomics - Delete Annotation Set
  x-api-slug: v1annotationsetsannotationsetid-delete
  description: |-
    Deletes an annotation set. Caller must have WRITE permission
    for the associated annotation set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsetsannotationsetid-delete-openapi.md
- name: Genomics - Get Annotation Set
  x-api-slug: v1annotationsetsannotationsetid-get
  description: |-
    Gets an annotation set. Caller must have READ permission for
    the associated dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsetsannotationsetid-get-openapi.md
- name: Genomics - Update Annotation Set
  x-api-slug: v1annotationsetsannotationsetid-put
  description: |-
    Updates an annotation set. The update must respect all mutability
    restrictions and other invariants described on the annotation set resource.
    Caller must have WRITE permission for the associated dataset.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1annotationsetsannotationsetid-put-openapi.md
- name: Genomics - Create Call Set
  x-api-slug: v1callsets-post
  description: |-
    Creates a new call set.

    For the definitions of call sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1callsets-post-openapi.md
- name: Genomics - Search Call Sets
  x-api-slug: v1callsetssearch-post
  description: |-
    Gets a list of call sets matching the criteria.

    For the definitions of call sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.searchCallSets](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/variantmethods.avdl#L178).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1callsetssearch-post-openapi.md
- name: Genomics - Delete Call Set
  x-api-slug: v1callsetscallsetid-delete
  description: |-
    Deletes a call set.

    For the definitions of call sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1callsetscallsetid-delete-openapi.md
- name: Genomics - Get Call Set
  x-api-slug: v1callsetscallsetid-get
  description: |-
    Gets a call set by ID.

    For the definitions of call sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1callsetscallsetid-get-openapi.md
- name: Genomics - Update Call Set
  x-api-slug: v1callsetscallsetid-patch
  description: |-
    Updates a call set.

    For the definitions of call sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1callsetscallsetid-patch-openapi.md
- name: Genomics - Get Datasets
  x-api-slug: v1datasets-get
  description: |-
    Lists datasets within a project.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasets-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasets-get-openapi.md
- name: Genomics - Create Dataset
  x-api-slug: v1datasets-post
  description: |-
    Creates a new dataset.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasets-post-openapi.md
- name: Genomics - Delete Dataset
  x-api-slug: v1datasetsdatasetid-delete
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasetsdatasetid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasetsdatasetid-delete-openapi.md
- name: Genomics - Get Dataset
  x-api-slug: v1datasetsdatasetid-get
  description: |-
    Gets a dataset by ID.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasetsdatasetid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasetsdatasetid-get-openapi.md
- name: Genomics - Update Dataset
  x-api-slug: v1datasetsdatasetid-patch
  description: |-
    Updates a dataset.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasetsdatasetid-patch-openapi.md
- name: Genomics - Restore Dataset
  x-api-slug: v1datasetsdatasetidundelete-post
  description: |-
    Undeletes a dataset by restoring a dataset which was deleted via this API.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    This operation is only possible for a week after the deletion occurred.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1datasetsdatasetidundelete-post-openapi.md
- name: Genomics - Search Read Group Sets
  x-api-slug: v1readgroupsetssearch-post
  description: |-
    Searches for read group sets matching the criteria.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.searchReadGroupSets](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/readmethods.avdl#L135).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetssearch-post-openapi.md
- name: Genomics - Delete Read Group Set
  x-api-slug: v1readgroupsetsreadgroupsetid-delete
  description: |-
    Deletes a read group set.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetsreadgroupsetid-delete-openapi.md
- name: Genomics - Get Read Group Set
  x-api-slug: v1readgroupsetsreadgroupsetid-get
  description: |-
    Gets a read group set by ID.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetsreadgroupsetid-get-openapi.md
- name: Genomics - Update Read Group Set
  x-api-slug: v1readgroupsetsreadgroupsetid-patch
  description: |-
    Updates a read group set.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    This method supports patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetsreadgroupsetid-patch-openapi.md
- name: Genomics - Get Coverage Buckets for Read Group Set
  x-api-slug: v1readgroupsetsreadgroupsetidcoveragebuckets-get
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetsreadgroupsetidcoveragebuckets-get-openapi.md
- name: Genomics - Export Read Group Set
  x-api-slug: v1readgroupsetsreadgroupsetidexport-post
  description: |-
    Exports a read group set to a BAM file in Google Cloud Storage.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Note that currently there may be some differences between exported BAM
    files and the original BAM file at the time of import. See
    ImportReadGroupSets
    for caveats.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetsreadgroupsetidexport-post-openapi.md
- name: Genomics - Create Read Group Set
  x-api-slug: v1readgroupsetsimport-post
  description: |-
    Creates read group sets by asynchronously importing the provided
    information.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    The caller must have WRITE permissions to the dataset.

    ## Notes on [BAM](https://samtools.github.io/hts-specs/SAMv1.pdf) import

    - Tags will be converted to strings - tag types are not preserved
    - Comments (`@CO`) in the input file header will not be preserved
    - Original header order of references (`@SQ`) will not be preserved
    - Any reverse stranded unmapped reads will be reverse complemented, and
    their qualities (also the "BQ" and "OQ" tags, if any) will be reversed
    - Unmapped reads will be stripped of positional information (reference name
    and position)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readgroupsetsimport-post-openapi.md
- name: Genomics - Search Reads
  x-api-slug: v1readssearch-post
  description: |-
    Gets a list of reads for one or more read group sets.

    For the definitions of read group sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Reads search operates over a genomic coordinate space of reference sequence
    & position defined over the reference sequences to which the requested
    read group sets are aligned.

    If a target positional range is specified, search returns all reads whose
    alignment to the reference genome overlap the range. A query which
    specifies only read group set IDs yields all reads in those read group
    sets, including unmapped reads.

    All reads returned (including reads on subsequent pages) are ordered by
    genomic coordinate (by reference sequence, then position). Reads with
    equivalent genomic coordinates are returned in an unspecified order. This
    order is consistent, such that two queries for the same content (regardless
    of page size) yield reads in the same order across their respective streams
    of paginated responses.

    Implements
    [GlobalAllianceApi.searchReads](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/readmethods.avdl#L85).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1readssearch-post-openapi.md
- name: Genomics - Search References
  x-api-slug: v1referencessearch-post
  description: |-
    Searches for references which match the given criteria.

    For the definitions of references and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.searchReferences](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/referencemethods.avdl#L146).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1referencessearch-post-openapi.md
- name: Genomics - Get Reference
  x-api-slug: v1referencesreferenceid-get
  description: |-
    Gets a reference.

    For the definitions of references and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.getReference](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/referencemethods.avdl#L158).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1referencesreferenceid-get-openapi.md
- name: Genomics - Get Reference Base
  x-api-slug: v1referencesreferenceidbases-get
  description: |-
    Lists the bases in a reference, optionally restricted to a range.

    For the definitions of references and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.getReferenceBases](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/referencemethods.avdl#L221).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1referencesreferenceidbases-get-openapi.md
- name: Genomics - Search Reference Set
  x-api-slug: v1referencesetssearch-post
  description: |-
    Searches for reference sets which match the given criteria.

    For the definitions of references and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.searchReferenceSets](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/referencemethods.avdl#L71)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1referencesetssearch-post-openapi.md
- name: Genomics - Get Reference Set
  x-api-slug: v1referencesetsreferencesetid-get
  description: |-
    Gets a reference set.

    For the definitions of references and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.getReferenceSet](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/referencemethods.avdl#L83).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1referencesetsreferencesetid-get-openapi.md
- name: Genomics - Create Variant
  x-api-slug: v1variants-post
  description: |-
    Creates a new variant.

    For the definitions of variants and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variants-post-openapi.md
- name: Genomics - Get Variants
  x-api-slug: v1variantssearch-post
  description: |-
    Gets a list of variants matching the criteria.

    For the definitions of variants and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.searchVariants](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/variantmethods.avdl#L126).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantssearch-post-openapi.md
- name: Genomics - Delete Variant
  x-api-slug: v1variantsvariantid-delete
  description: |-
    Deletes a variant.

    For the definitions of variants and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsvariantid-delete-openapi.md
- name: Genomics - Get Variant
  x-api-slug: v1variantsvariantid-get
  description: |-
    Gets a variant by ID.

    For the definitions of variants and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsvariantid-get-openapi.md
- name: Genomics - Update Variant
  x-api-slug: v1variantsvariantid-patch
  description: |-
    Updates a variant.

    For the definitions of variants and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    This method supports patch semantics. Returns the modified variant without
    its calls.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsvariantid-patch-openapi.md
- name: Genomics - Create Variant
  x-api-slug: v1variantsimport-post
  description: |-
    Creates variant data by asynchronously importing the provided information.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    The variants for import will be merged with any existing variant that
    matches its reference sequence, start, end, reference bases, and
    alternative bases. If no such variant exists, a new one will be created.

    When variants are merged, the call information from the new variant
    is added to the existing variant, and Variant info fields are merged
    as specified in
    infoMergeConfig.
    As a special case, for single-sample VCF files, QUAL and FILTER fields will
    be moved to the call level; these are sometimes interpreted in a
    call-specific context.
    Imported VCF headers are appended to the metadata already in a variant set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsimport-post-openapi.md
- name: Genomics - Merge Variants
  x-api-slug: v1variantsmerge-post
  description: |-
    Merges the given variants with existing variants.

    For the definitions of variants and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Each variant will be
    merged with an existing variant that matches its reference sequence,
    start, end, reference bases, and alternative bases. If no such variant
    exists, a new one will be created.

    When variants are merged, the call information from the new variant
    is added to the existing variant. Variant info fields are merged as
    specified in the
    infoMergeConfig
    field of the MergeVariantsRequest.

    Please exercise caution when using this method!  It is easy to introduce
    mistakes in existing variants and difficult to back out of them.  For
    example,
    suppose you were trying to merge a new variant with an existing one and
    both
    variants contain calls that belong to callsets with the same callset ID.

        // Existing variant - irrelevant fields trimmed for clarity
        {
            "variantSetId": "10473108253681171589",
            "referenceName": "1",
            "start": "10582",
            "referenceBases": "G",
            "alternateBases": [
                "A"
            ],
            "calls": [
                {
                    "callSetId": "10473108253681171589-0",
                    "callSetName": "CALLSET0",
                    "genotype": [
                        0,
                        1
                    ],
                }
            ]
        }

        // New variant with conflicting call information
        {
            "variantSetId": "10473108253681171589",
            "referenceName": "1",
            "start": "10582",
            "referenceBases": "G",
            "alternateBases": [
                "A"
            ],
            "calls": [
                {
                    "callSetId": "10473108253681171589-0",
                    "callSetName": "CALLSET0",
                    "genotype": [
                        1,
                        1
                    ],
                }
            ]
        }

    The resulting merged variant would overwrite the existing calls with those
    from the new variant:

        {
            "variantSetId": "10473108253681171589",
            "referenceName": "1",
            "start": "10582",
            "referenceBases": "G",
            "alternateBases": [
                "A"
            ],
            "calls": [
                {
                    "callSetId": "10473108253681171589-0",
                    "callSetName": "CALLSET0",
                    "genotype": [
                        1,
                        1
                    ],
                }
            ]
        }

    This may be the desired outcome, but it is up to the user to determine if
    if that is indeed the case.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsmerge-post-openapi.md
- name: Genomics - Create Variant Set
  x-api-slug: v1variantsets-post
  description: |-
    Creates a new variant set.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    The provided variant set must have a valid `datasetId` set - all other
    fields are optional. Note that the `id` field will be ignored, as this is
    assigned by the server.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsets-post-openapi.md
- name: Genomics - Get Variant Sets
  x-api-slug: v1variantsetssearch-post
  description: |-
    Returns a list of all variant sets matching search criteria.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    Implements
    [GlobalAllianceApi.searchVariantSets](https://github.com/ga4gh/schemas/blob/v0.5.1/src/main/resources/avro/variantmethods.avdl#L49).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsetssearch-post-openapi.md
- name: Genomics - Delete Variant Set
  x-api-slug: v1variantsetsvariantsetid-delete
  description: |-
    Deletes a variant set including all variants, call sets, and calls within.
    This is not reversible.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsetsvariantsetid-delete-openapi.md
- name: Genomics - Get Variant Set
  x-api-slug: v1variantsetsvariantsetid-get
  description: |-
    Gets a variant set by ID.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsetsvariantsetid-get-openapi.md
- name: Genomics - Update Variant Set
  x-api-slug: v1variantsetsvariantsetid-patch
  description: |-
    Updates a variant set using patch semantics.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsetsvariantsetid-patch-openapi.md
- name: Genomics - Export Variant Set
  x-api-slug: v1variantsetsvariantsetidexport-post
  description: |-
    Exports variant set data to an external destination.

    For the definitions of variant sets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1variantsetsvariantsetidexport-post-openapi.md
- name: Genomics - Get Operation
  x-api-slug: v1name-get
  description: |-
    Gets the latest state of a long-running operation.  Clients can use this
    method to poll the operation result at intervals as recommended by the API
    service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1name-get-openapi.md
- name: Genomics - Cancel Operation
  x-api-slug: v1namecancel-post
  description: Starts asynchronous cancellation on a long-running operation. The server
    makes a best effort to cancel the operation, but success is not guaranteed. Clients
    may use Operations.GetOperation or Operations.ListOperations to check whether
    the cancellation succeeded or the operation completed despite cancellation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1namecancel-post-openapi.md
- name: Genomics - Get IAM Policy
  x-api-slug: v1resourcegetiampolicy-post
  description: |-
    Gets the access control policy for the dataset. This is empty if the
    policy or resource does not exist.

    See <a href="/iam/docs/managing-policies#getting_a_policy">Getting a
    Policy</a> for more information.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1resourcegetiampolicy-post-openapi.md
- name: Genomics - Set IAM Policy
  x-api-slug: v1resourcesetiampolicy-post
  description: |-
    Sets the access control policy on the specified dataset. Replaces any
    existing policy.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)

    See <a href="/iam/docs/managing-policies#setting_a_policy">Setting a
    Policy</a> for more information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1resourcesetiampolicy-post-openapi.md
- name: Genomics - Test IAM Permissions
  x-api-slug: v1resourcetestiampermissions-post
  description: |-
    Returns permissions that a caller has on the specified resource.
    See <a href="/iam/docs/managing-policies#testing_permissions">Testing
    Permissions</a> for more information.

    For the definitions of datasets and other genomics resources, see
    [Fundamentals of Google
    Genomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/power-your-science.png
  humanURL: https://cloud.google.com/genomics/
  baseURL: ://genomics.googleapis.com//
  tags: Science, Genome, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-genomics/master/_listings/google-genomics/v1resourcetestiampermissions-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.fusion.tables.api.gallery.streamdata.io
- type: x-api-stack
  url: http://google.genomics.stack.network
- type: x-documentation
  url: https://cloud.google.com/genomics/overview
- type: x-forum
  url: https://groups.google.com/forum/#!forum/google-genomics-discuss/join
- type: x-pricing
  url: https://cloud.google.com/genomics/pricing
- type: x-rate-limits
  url: https://cloud.google.com/genomics/quotas
- type: x-support
  url: https://cloud.google.com/genomics/support
- type: x-website
  url: https://cloud.google.com/genomics/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---