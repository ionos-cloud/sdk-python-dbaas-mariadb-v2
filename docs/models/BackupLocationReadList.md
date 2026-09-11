# BackupLocationReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | The offset specified in the request (if none was specified, the default offset is 0).  | [readonly] 
**limit** | **int** | The limit specified in the request (if none was specified, use the endpoint&#39;s default pagination limit).  | [readonly] 
**links** | [**Links**](Links.md) |  | 
**id** | **str** | ID of the list of BackupLocation resources. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the list of BackupLocation resources. | 
**items** | [**list[BackupLocationRead]**](BackupLocationRead.md) | The list of BackupLocation resources. | [optional] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.backup_location_read_list import BackupLocationReadList

# TODO update the JSON string below
json = "{}"
# create an instance of BackupLocationReadList from a JSON string
backup_location_read_list_instance = BackupLocationReadList.from_json(json)
# print the JSON string representation of the object
print(BackupLocationReadList.to_json())

# convert the object into a dict
backup_location_read_list_dict = backup_location_read_list_instance.to_dict()
# create an instance of BackupLocationReadList from a dict
backup_location_read_list_from_dict = BackupLocationReadList.from_dict(backup_location_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


