##### exist语法

```
GET tjga-case-test/_search
{
  "timeout": "60s",
  "query": {
    "bool": {
      "must_not": [
        {
          "exists": {
            "field": "personInfoList.familyMemberList"
          }
        }
      ]
    }
  }
}
```

