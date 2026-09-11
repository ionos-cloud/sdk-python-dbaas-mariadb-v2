# Metadata

Metadata of the resource.

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

## Example

```python
from ionoscloud_dbaas_mariadb.models.metadata import Metadata

# TODO update the JSON string below
json = "{}"
# create an instance of Metadata from a JSON string
metadata_instance = Metadata.from_json(json)
# print the JSON string representation of the object
print(Metadata.to_json())

# convert the object into a dict
metadata_dict = metadata_instance.to_dict()
# create an instance of Metadata from a dict
metadata_from_dict = Metadata.from_dict(metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


