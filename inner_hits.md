##### 返回`nested object` 或者 子文档，配合has_child 或nested 使用

```
GET case-document-test.2019/_search
{
  "query": {
    "bool": {
      "must": [
        {
          "nested": {
            "path": "personNestedList",
            "query": {
              "term": {
                "personNestedList.keyCode": {
                  "value": "SARY"
                }
              }
            },
            "inner_hits": {}
          }
        },
        {
          "match": {
            "docInfo.documentCode": "XZ-GAXZCF-JDS"
          }
        }
      ]
    }
  }, "_source": ["inner_hits.personNestedList.hits"]
```



