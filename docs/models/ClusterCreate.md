# ClusterCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**ClusterCreateProperties**](ClusterCreateProperties.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster_create import ClusterCreate

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterCreate from a JSON string
cluster_create_instance = ClusterCreate.from_json(json)
# print the JSON string representation of the object
print(ClusterCreate.to_json())

# convert the object into a dict
cluster_create_dict = cluster_create_instance.to_dict()
# create an instance of ClusterCreate from a dict
cluster_create_from_dict = ClusterCreate.from_dict(cluster_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


