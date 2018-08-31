{
  "info": {
    "name": "Google Genomics API Get Datasets",
    "_postman_id": "f997b089-63a3-4615-b662-d05c7e8de178",
    "description": "Lists datasets within a project.\n\nFor the definitions of datasets and other genomics resources, see\n[Fundamentals of Google\nGenomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dataset",
      "item": [
        {
          "id": "04767eaa-637b-4f82-abc9-7449ea10eaa3",
          "name": "genomics.datasets.list",
          "request": {
            "url": "http://genomics.googleapis.com/v1/datasets?pageSize=%7B%7D&pageToken=%7B%7D&projectId=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists datasets within a project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3674757d-e5d9-45df-aaef-cf22dda257d9"
            }
          ]
        }
      ]
    }
  ]
}