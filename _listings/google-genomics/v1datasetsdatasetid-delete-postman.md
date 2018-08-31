{
  "info": {
    "name": "Google Genomics API Delete Dataset",
    "_postman_id": "eea9305a-d229-43d6-94bc-1c117d97527c",
    "description": "Deletes a dataset and all of its contents (all read group sets,\nreference sets, variant sets, call sets, annotation sets, etc.)\nThis is reversible (up to one week after the deletion) via\nthe\ndatasets.undelete\noperation.\n\nFor the definitions of datasets and other genomics resources, see\n[Fundamentals of Google\nGenomics](https://cloud.google.com/genomics/fundamentals-of-google-genomics)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dataset",
      "item": [
        {
          "id": "f89e0c45-f3df-4151-9a0f-1b9231562740",
          "name": "genomics.datasets.delete",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a dataset and all of its contents (all read group sets,\nreference sets, variant sets, call sets, annotation sets, etc"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59e00b97-7ecc-4602-8dfe-17305675191f"
            }
          ]
        }
      ]
    }
  ]
}