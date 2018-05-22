{
  "info": {
    "name": "Google Genomics API Get Dataset",
    "_postman_id": "4c047e60-c3f5-4fe8-95b6-b811ff6639bb",
    "description": "Gets a dataset by ID.\n\nFor the definitions of datasets and other genomics resources, see\n[Fundamentals of Google\nGenomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dataset",
      "item": [
        {
          "id": "9d7f25dd-3c81-4833-b9c0-f5e48da9d3dc",
          "name": "genomics.datasets.get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "genomics.googleapis.com",
              "path": [
                "v1/datasets/:datasetId"
              ],
              "variable": [
                {
                  "id": "datasetId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a dataset by ID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "976d846f-2fd2-48a1-b8dc-f51cdf9c0350"
            }
          ]
        }
      ]
    }
  ]
}