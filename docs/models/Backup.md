# Backup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cluster_id** | **str** | The unique identifier of the cluster this backup belongs to. | [optional] 
**cluster_name** | **str** | The name of the MariaDB cluster this backup belongs to. | [optional] [readonly] 
**mariadb_cluster_version** | **str** | The MariaDB version of the cluster at backup time. | [optional] 
**earliest_recovery_target_time** | **datetime** | The earliest point in time to which the cluster can be restored from this backup. | [optional] 
**latest_recovery_target_time** | **datetime** | The latest possible point in time to which the cluster can be restored. If the backup can be restored up to the current time, this field will be null.  | [optional] 
**location** | **str** | The Object Storage location where the backup will be created. The BackupLocations provides a list of supported locations.  | [optional] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.backup import Backup

# TODO update the JSON string below
json = "{}"
# create an instance of Backup from a JSON string
backup_instance = Backup.from_json(json)
# print the JSON string representation of the object
print(Backup.to_json())

# convert the object into a dict
backup_dict = backup_instance.to_dict()
# create an instance of Backup from a dict
backup_from_dict = Backup.from_dict(backup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


