# BackupEnsure


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Backup. | 
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**Backup**](Backup.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.backup_ensure import BackupEnsure

# TODO update the JSON string below
json = "{}"
# create an instance of BackupEnsure from a JSON string
backup_ensure_instance = BackupEnsure.from_json(json)
# print the JSON string representation of the object
print(BackupEnsure.to_json())

# convert the object into a dict
backup_ensure_dict = backup_ensure_instance.to_dict()
# create an instance of BackupEnsure from a dict
backup_ensure_from_dict = BackupEnsure.from_dict(backup_ensure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


