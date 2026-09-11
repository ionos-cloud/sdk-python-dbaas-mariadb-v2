# ClusterMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_date** | **datetime** | The ISO 8601 creation timestamp. | [optional] [readonly] 
**created_by** | **str** | Unique name of the identity that created the resource. | [optional] [readonly] 
**created_by_user_id** | **str** | Unique id of the identity that created the resource. | [optional] [readonly] 
**last_modified_date** | **datetime** | The ISO 8601 modified timestamp. | [optional] [readonly] 
**last_modified_by** | **str** | Unique name of the identity that last modified the resource. | [optional] [readonly] 
**last_modified_by_user_id** | **str** | Unique id of the identity that last modified the resource. | [optional] [readonly] 
**resource_urn** | **str** | Unique name of the resource. | [optional] [readonly] 
**state** | [**MariadbClusterStates**](MariadbClusterStates.md) |  | [optional] 
**status_message** | **str** | A human-readable message describing the current state. Populated when &#x60;state&#x60; is &#x60;FAILED&#x60;. | [optional] [readonly] 
**dns_name** | **str** | The DNS name used to access the cluster. | [optional] [readonly] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster_metadata import ClusterMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterMetadata from a JSON string
cluster_metadata_instance = ClusterMetadata.from_json(json)
# print the JSON string representation of the object
print(ClusterMetadata.to_json())

# convert the object into a dict
cluster_metadata_dict = cluster_metadata_instance.to_dict()
# create an instance of ClusterMetadata from a dict
cluster_metadata_from_dict = ClusterMetadata.from_dict(cluster_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


