# MariadbRestoreClusterFromBackup

Restores the cluster from a backup. On cluster creation, set `sourceBackupId` (optionally `recoveryTargetDatetime`) to initialize the new cluster from an existing backup. On in-place modification, set `recoveryTargetDatetime` only; the restore source is inferred from the cluster's own backups. The current data is overwritten with the restored data, and the cluster may experience a brief period of downtime during this process. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_backup_id** | **str** | UUID of the backup to restore from. Required for restore on cluster creation; not valid for in-place restore, where the source is inferred from the cluster&#39;s own backups.  | [optional] 
**recovery_target_datetime** | **datetime** | Providing this value as an ISO 8601 timestamp causes the system to replay the backups up to the specified time. Optional on cluster creation (the backup is applied in its entirety if omitted); required for in-place restore.  | [optional] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.mariadb_restore_cluster_from_backup import MariadbRestoreClusterFromBackup

# TODO update the JSON string below
json = "{}"
# create an instance of MariadbRestoreClusterFromBackup from a JSON string
mariadb_restore_cluster_from_backup_instance = MariadbRestoreClusterFromBackup.from_json(json)
# print the JSON string representation of the object
print(MariadbRestoreClusterFromBackup.to_json())

# convert the object into a dict
mariadb_restore_cluster_from_backup_dict = mariadb_restore_cluster_from_backup_instance.to_dict()
# create an instance of MariadbRestoreClusterFromBackup from a dict
mariadb_restore_cluster_from_backup_from_dict = MariadbRestoreClusterFromBackup.from_dict(mariadb_restore_cluster_from_backup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


