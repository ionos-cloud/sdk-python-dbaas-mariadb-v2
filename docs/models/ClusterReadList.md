# ClusterReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | The offset specified in the request (if none was specified, the default offset is 0).  | [readonly] 
**limit** | **int** | The limit specified in the request (if none was specified, use the endpoint&#39;s default pagination limit).  | [readonly] 
**links** | [**Links**](Links.md) |  | 
**id** | **str** | ID of the list of Cluster resources. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the list of Cluster resources. | 
**items** | [**list[ClusterRead]**](ClusterRead.md) | The list of Cluster resources. | [optional] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster_read_list import ClusterReadList

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterReadList from a JSON string
cluster_read_list_instance = ClusterReadList.from_json(json)
# print the JSON string representation of the object
print(ClusterReadList.to_json())

# convert the object into a dict
cluster_read_list_dict = cluster_read_list_instance.to_dict()
# create an instance of ClusterReadList from a dict
cluster_read_list_from_dict = ClusterReadList.from_dict(cluster_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


