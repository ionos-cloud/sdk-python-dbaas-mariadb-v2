# BackupRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Backup. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Backup. | 
**metadata** | **object** |  | [readonly] 
**properties** | [**Backup**](Backup.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.backup_read import BackupRead

# TODO update the JSON string below
json = "{}"
# create an instance of BackupRead from a JSON string
backup_read_instance = BackupRead.from_json(json)
# print the JSON string representation of the object
print(BackupRead.to_json())

# convert the object into a dict
backup_read_dict = backup_read_instance.to_dict()
# create an instance of BackupRead from a dict
backup_read_from_dict = BackupRead.from_dict(backup_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


