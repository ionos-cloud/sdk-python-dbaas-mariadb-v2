# ClusterEnsure


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Cluster. | 
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**Cluster**](Cluster.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster_ensure import ClusterEnsure

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterEnsure from a JSON string
cluster_ensure_instance = ClusterEnsure.from_json(json)
# print the JSON string representation of the object
print(ClusterEnsure.to_json())

# convert the object into a dict
cluster_ensure_dict = cluster_ensure_instance.to_dict()
# create an instance of ClusterEnsure from a dict
cluster_ensure_from_dict = ClusterEnsure.from_dict(cluster_ensure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


