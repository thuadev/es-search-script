##### first step

```
POST case-document-test.2019/_search?scroll=1m
{
  "query": {
    "match_all": {}
  },
  "sort": [
    {
      "docInfo.documentCreateTime": {
        "order": "desc"
      }
    }
  ]
}
```

##### second step

```
POST /_search/scroll
{
  "scroll": "1m",
  "scroll_id": "DnF1ZXJ5VGhlbkZldGNoBQAAAAABW0_SFjNaNy1panVNUTZ1V1Y2eFBQTk1UOVEAAAAAAVtPzhYzWjctaWp1TVE2dVdWNnhQUE5NVDlRAAAAAAFbT88WM1o3LWlqdU1RNnVXVjZ4UFBOTVQ5UQAAAAABW0_RFjNaNy1panVNUTZ1V1Y2eFBQTk1UOVEAAAAAAVtP0BYzWjctaWp1TVE2dVdWNnhQUE5NVDlR"
}
```


