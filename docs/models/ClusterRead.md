# ClusterRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Cluster. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Cluster. | 
**metadata** | [**ClusterMetadata**](ClusterMetadata.md) |  | 
**properties** | [**Cluster**](Cluster.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster_read import ClusterRead

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterRead from a JSON string
cluster_read_instance = ClusterRead.from_json(json)
# print the JSON string representation of the object
print(ClusterRead.to_json())

# convert the object into a dict
cluster_read_dict = cluster_read_instance.to_dict()
# create an instance of ClusterRead from a dict
cluster_read_from_dict = ClusterRead.from_dict(cluster_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


