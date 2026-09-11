# ClusterBackup

Configures backup location and retention

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**location** | **str** | The Object Storage location where the backup will be created. The BackupLocations provides a list of supported locations.  | 
**retention_days** | **int** | Configures how many days cluster backups are retained. | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster_backup import ClusterBackup

# TODO update the JSON string below
json = "{}"
# create an instance of ClusterBackup from a JSON string
cluster_backup_instance = ClusterBackup.from_json(json)
# print the JSON string representation of the object
print(ClusterBackup.to_json())

# convert the object into a dict
cluster_backup_dict = cluster_backup_instance.to_dict()
# create an instance of ClusterBackup from a dict
cluster_backup_from_dict = ClusterBackup.from_dict(cluster_backup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


