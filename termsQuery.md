##### termsQuery

```
GET tjga-case-test/_search
{
  "timeout": "60s",
  "query": {
    "bool": {
      "must": [
        {
          "terms": {
            "caseNum": [
              "A1201024200002020040019",
              "A1201024200002020040058",
              "F1201135300002020010004",
              "Z1201024200002020030092",
              "Z1201024500002019125004",
              "Z1201114700002019115014",
              "Z1201135300002019125004"
            ],
            "boost": 1
          }
        }
      ],
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

