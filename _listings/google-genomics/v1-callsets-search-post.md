---
swagger: "2.0"
info:
  title: Genomics
  description: Upload, process, query, and search Genomics data in the cloud.
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
  /v1/callsets/search:
    post:
      summary: Search Call Sets
      description: Gets a list of call sets matching the criteria
      operationId: genomics.callsets.search
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - call set
definitions:
  Annotation:
    properties:
      annotationSetId:
        description: This is a default description.
        type: post
      end:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      referenceId:
        description: This is a default description.
        type: post
      referenceName:
        description: This is a default description.
        type: post
      reverseStrand:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  AnnotationSet:
    properties:
      datasetId:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
      sourceUri:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  BatchCreateAnnotationsRequest:
    properties:
      annotations:
        description: This is a default description.
        type: post
      requestId:
        description: This is a default description.
        type: post
  BatchCreateAnnotationsResponse:
    properties:
      entries:
        description: This is a default description.
        type: post
  Binding:
    properties:
      members:
        description: This is a default description.
        type: post
      role:
        description: This is a default description.
        type: post
  CallSet:
    properties:
      created:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      sampleId:
        description: This is a default description.
        type: post
      variantSetIds:
        description: This is a default description.
        type: post
  CancelOperationRequest:
    properties: []
  CigarUnit:
    properties:
      operation:
        description: This is a default description.
        type: post
      operationLength:
        description: This is a default description.
        type: post
      referenceSequence:
        description: This is a default description.
        type: post
  ClinicalCondition:
    properties:
      conceptId:
        description: This is a default description.
        type: post
      externalIds:
        description: This is a default description.
        type: post
      names:
        description: This is a default description.
        type: post
      omimId:
        description: This is a default description.
        type: post
  CodingSequence:
    properties:
      end:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
  ComputeEngine:
    properties:
      diskNames:
        description: This is a default description.
        type: post
      instanceName:
        description: This is a default description.
        type: post
      machineType:
        description: This is a default description.
        type: post
      zone:
        description: This is a default description.
        type: post
  CoverageBucket:
    properties:
      meanCoverage:
        description: This is a default description.
        type: post
  Dataset:
    properties:
      createTime:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      projectId:
        description: This is a default description.
        type: post
  Empty:
    properties: []
  Entry:
    properties: []
  Exon:
    properties:
      end:
        description: This is a default description.
        type: post
      frame:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
  Experiment:
    properties:
      instrumentModel:
        description: This is a default description.
        type: post
      libraryId:
        description: This is a default description.
        type: post
      platformUnit:
        description: This is a default description.
        type: post
      sequencingCenter:
        description: This is a default description.
        type: post
  ExportReadGroupSetRequest:
    properties:
      exportUri:
        description: This is a default description.
        type: post
      projectId:
        description: This is a default description.
        type: post
      referenceNames:
        description: This is a default description.
        type: post
  ExportVariantSetRequest:
    properties:
      bigqueryDataset:
        description: This is a default description.
        type: post
      bigqueryTable:
        description: This is a default description.
        type: post
      callSetIds:
        description: This is a default description.
        type: post
      format:
        description: This is a default description.
        type: post
      projectId:
        description: This is a default description.
        type: post
  ExternalId:
    properties:
      id:
        description: This is a default description.
        type: post
      sourceName:
        description: This is a default description.
        type: post
  GetIamPolicyRequest:
    properties: []
  ImportReadGroupSetsRequest:
    properties:
      datasetId:
        description: This is a default description.
        type: post
      partitionStrategy:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
      sourceUris:
        description: This is a default description.
        type: post
  ImportReadGroupSetsResponse:
    properties:
      readGroupSetIds:
        description: This is a default description.
        type: post
  ImportVariantsRequest:
    properties:
      format:
        description: This is a default description.
        type: post
      infoMergeConfig:
        description: This is a default description.
        type: post
      normalizeReferenceNames:
        description: This is a default description.
        type: post
      sourceUris:
        description: This is a default description.
        type: post
      variantSetId:
        description: This is a default description.
        type: post
  ImportVariantsResponse:
    properties:
      callSetIds:
        description: This is a default description.
        type: post
  LinearAlignment:
    properties:
      cigar:
        description: This is a default description.
        type: post
      mappingQuality:
        description: This is a default description.
        type: post
  ListBasesResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      offset:
        description: This is a default description.
        type: post
      sequence:
        description: This is a default description.
        type: post
  ListCoverageBucketsResponse:
    properties:
      bucketWidth:
        description: This is a default description.
        type: post
      coverageBuckets:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListDatasetsResponse:
    properties:
      datasets:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListOperationsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      operations:
        description: This is a default description.
        type: post
  MergeVariantsRequest:
    properties:
      infoMergeConfig:
        description: This is a default description.
        type: post
      variantSetId:
        description: This is a default description.
        type: post
      variants:
        description: This is a default description.
        type: post
  Operation:
    properties:
      done:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      response:
        description: This is a default description.
        type: post
  OperationEvent:
    properties:
      description:
        description: This is a default description.
        type: post
      endTime:
        description: This is a default description.
        type: post
      startTime:
        description: This is a default description.
        type: post
  OperationMetadata:
    properties:
      clientId:
        description: This is a default description.
        type: post
      createTime:
        description: This is a default description.
        type: post
      endTime:
        description: This is a default description.
        type: post
      events:
        description: This is a default description.
        type: post
      labels:
        description: This is a default description.
        type: post
      projectId:
        description: This is a default description.
        type: post
      request:
        description: This is a default description.
        type: post
      runtimeMetadata:
        description: This is a default description.
        type: post
      startTime:
        description: This is a default description.
        type: post
  Policy:
    properties:
      bindings:
        description: This is a default description.
        type: post
      etag:
        description: This is a default description.
        type: post
      version:
        description: This is a default description.
        type: post
  Position:
    properties:
      position:
        description: This is a default description.
        type: post
      referenceName:
        description: This is a default description.
        type: post
      reverseStrand:
        description: This is a default description.
        type: post
  Program:
    properties:
      commandLine:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      prevProgramId:
        description: This is a default description.
        type: post
      version:
        description: This is a default description.
        type: post
  Range:
    properties:
      end:
        description: This is a default description.
        type: post
      referenceName:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
  Read:
    properties:
      alignedQuality:
        description: This is a default description.
        type: post
      alignedSequence:
        description: This is a default description.
        type: post
      duplicateFragment:
        description: This is a default description.
        type: post
      failedVendorQualityChecks:
        description: This is a default description.
        type: post
      fragmentLength:
        description: This is a default description.
        type: post
      fragmentName:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      numberReads:
        description: This is a default description.
        type: post
      properPlacement:
        description: This is a default description.
        type: post
  ReadGroup:
    properties:
      datasetId:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      predictedInsertSize:
        description: This is a default description.
        type: post
      programs:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
      sampleId:
        description: This is a default description.
        type: post
  ReadGroupSet:
    properties:
      datasetId:
        description: This is a default description.
        type: post
      filename:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      readGroups:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
  Reference:
    properties:
      id:
        description: This is a default description.
        type: post
      length:
        description: This is a default description.
        type: post
      md5checksum:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      ncbiTaxonId:
        description: This is a default description.
        type: post
      sourceAccessions:
        description: This is a default description.
        type: post
      sourceUri:
        description: This is a default description.
        type: post
  ReferenceBound:
    properties:
      referenceName:
        description: This is a default description.
        type: post
      upperBound:
        description: This is a default description.
        type: post
  ReferenceSet:
    properties:
      assemblyId:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      md5checksum:
        description: This is a default description.
        type: post
      ncbiTaxonId:
        description: This is a default description.
        type: post
      referenceIds:
        description: This is a default description.
        type: post
      sourceAccessions:
        description: This is a default description.
        type: post
      sourceUri:
        description: This is a default description.
        type: post
  RuntimeMetadata:
    properties: []
  SearchAnnotationSetsRequest:
    properties:
      datasetIds:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
      types:
        description: This is a default description.
        type: post
  SearchAnnotationSetsResponse:
    properties:
      annotationSets:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  SearchAnnotationsRequest:
    properties:
      annotationSetIds:
        description: This is a default description.
        type: post
      end:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
      referenceId:
        description: This is a default description.
        type: post
      referenceName:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
  SearchAnnotationsResponse:
    properties:
      annotations:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  SearchCallSetsRequest:
    properties:
      name:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
      variantSetIds:
        description: This is a default description.
        type: post
  SearchCallSetsResponse:
    properties:
      callSets:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  SearchReadGroupSetsRequest:
    properties:
      datasetIds:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
  SearchReadGroupSetsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      readGroupSets:
        description: This is a default description.
        type: post
  SearchReadsRequest:
    properties:
      end:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
      readGroupIds:
        description: This is a default description.
        type: post
      readGroupSetIds:
        description: This is a default description.
        type: post
      referenceName:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
  SearchReadsResponse:
    properties:
      alignments:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  SearchReferenceSetsRequest:
    properties:
      accessions:
        description: This is a default description.
        type: post
      assemblyId:
        description: This is a default description.
        type: post
      md5checksums:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
  SearchReferenceSetsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      referenceSets:
        description: This is a default description.
        type: post
  SearchReferencesRequest:
    properties:
      accessions:
        description: This is a default description.
        type: post
      md5checksums:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
  SearchReferencesResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      references:
        description: This is a default description.
        type: post
  SearchVariantSetsRequest:
    properties:
      datasetIds:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
  SearchVariantSetsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      variantSets:
        description: This is a default description.
        type: post
  SearchVariantsRequest:
    properties:
      callSetIds:
        description: This is a default description.
        type: post
      end:
        description: This is a default description.
        type: post
      maxCalls:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
      referenceName:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
      variantName:
        description: This is a default description.
        type: post
      variantSetIds:
        description: This is a default description.
        type: post
  SearchVariantsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      variants:
        description: This is a default description.
        type: post
  SetIamPolicyRequest:
    properties: []
  Status:
    properties:
      code:
        description: This is a default description.
        type: post
      details:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
  TestIamPermissionsRequest:
    properties:
      permissions:
        description: This is a default description.
        type: post
  TestIamPermissionsResponse:
    properties:
      permissions:
        description: This is a default description.
        type: post
  Transcript:
    properties:
      exons:
        description: This is a default description.
        type: post
      geneId:
        description: This is a default description.
        type: post
  UndeleteDatasetRequest:
    properties: []
  Variant:
    properties:
      alternateBases:
        description: This is a default description.
        type: post
      calls:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      end:
        description: This is a default description.
        type: post
      filter:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      names:
        description: This is a default description.
        type: post
      quality:
        description: This is a default description.
        type: post
      referenceBases:
        description: This is a default description.
        type: post
  VariantAnnotation:
    properties:
      alternateBases:
        description: This is a default description.
        type: post
      clinicalSignificance:
        description: This is a default description.
        type: post
      conditions:
        description: This is a default description.
        type: post
      effect:
        description: This is a default description.
        type: post
      geneId:
        description: This is a default description.
        type: post
      transcriptIds:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  VariantCall:
    properties:
      callSetId:
        description: This is a default description.
        type: post
      callSetName:
        description: This is a default description.
        type: post
      genotype:
        description: This is a default description.
        type: post
      genotypeLikelihood:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      phaseset:
        description: This is a default description.
        type: post
  VariantSet:
    properties:
      datasetId:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      referenceBounds:
        description: This is a default description.
        type: post
      referenceSetId:
        description: This is a default description.
        type: post
  VariantSetMetadata:
    properties:
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      info:
        description: This is a default description.
        type: post
      key:
        description: This is a default description.
        type: post
      number:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
x-collection-name: Google Genomics
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