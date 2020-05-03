##### 查询nested字段

```
GET case-document-test.2019/_search
{
  "query": {
    "bool": {
      "must": [
        {
          "nested": {
            "path": "propertyNestedList",
            "query": {
              "term": {
                "propertyNestedList.keyCode": {
                  "value": "SADJB.WH"
                }
              }
            }
          }
        }
      ]
    }
  }
}
```

