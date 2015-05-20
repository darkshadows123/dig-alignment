## cluster-similarity-sample.json

### PyTransforms
#### _cluster_uri_
From column: _Column_1_
>``` python
uri = cluster_body_uri(getValue("Column_1"))
if uri:
   return getHTBaseUrl() + uri
return ''
```

#### _cluster2_uri_
From column: _Column_2_
>``` python
return cluster_body_uri(getValue("Column_2"))
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Column_2_ | `rdfs:label` | `memex:Cluster1`|
| _Column_3_ | `memex:similarity_score` | `memex:SimilarObject1`|
| _Column_5_ | `memex:numberOfItems` | `memex:Cluster1`|
| _cluster2_uri_ | `uri` | `memex:Cluster1`|
| _cluster_uri_ | `memex:similar_url` | `memex:SimilarObject1`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `memex:Cluster1` | `schema:isSimilarTo` | `memex:SimilarObject1`|