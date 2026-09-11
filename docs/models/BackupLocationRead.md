# BackupLocationRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the BackupLocation. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the BackupLocation. | 
**metadata** | **object** |  | [readonly] 
**properties** | [**BackupLocation**](BackupLocation.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.backup_location_read import BackupLocationRead

# TODO update the JSON string below
json = "{}"
# create an instance of BackupLocationRead from a JSON string
backup_location_read_instance = BackupLocationRead.from_json(json)
# print the JSON string representation of the object
print(BackupLocationRead.to_json())

# convert the object into a dict
backup_location_read_dict = backup_location_read_instance.to_dict()
# create an instance of BackupLocationRead from a dict
backup_location_read_from_dict = BackupLocationRead.from_dict(backup_location_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


