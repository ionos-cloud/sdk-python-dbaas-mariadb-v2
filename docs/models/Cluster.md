# Cluster

Create, manage, and monitor MariaDB clusters through the IONOS CLOUD API. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The name of your MariaDB cluster. Must be 63 characters or less and must begin and end with an alphanumeric character (&#x60;[a-z0-9A-Z]&#x60;) with dashes (&#x60;-&#x60;), underscores (&#x60;_&#x60;), dots (&#x60;.&#x60;), and alphanumerics between.  | 
**description** | **str** | Human-readable description for the cluster. | [optional] 
**version** | **str** | The MariaDB version for the cluster. Use GET /versions to retrieve the list of supported versions. To upgrade, provide a version listed in canUpgradeTo for the current version. Downgrades are not supported.  | 
**instances** | [**InstanceConfiguration**](InstanceConfiguration.md) |  | 
**connection** | [**MariadbClusterConnection**](MariadbClusterConnection.md) |  | 
**maintenance_window** | [**MaintenanceWindow**](MaintenanceWindow.md) |  | 
**credentials** | [**MariadbUser**](MariadbUser.md) |  | [optional] 
**restore_from_backup** | [**MariadbRestoreClusterFromBackup**](MariadbRestoreClusterFromBackup.md) |  | [optional] 
**logs_enabled** | **bool** | Allows or disallows the collection and reporting of logs for this cluster&#39;s observability. If the observability service is not activated on the contract, this setting is accepted but has no effect; log collection will not be enabled until the observability service is activated.  | [optional] [default to False]
**metrics_enabled** | **bool** | Allows or disallows the collection and reporting of metrics for this cluster&#39;s observability. If the observability service is not activated on the contract, this setting is accepted but has no effect; metric collection will not be enabled until the observability service is activated.  | [optional] [default to False]
**backup** | [**ClusterBackup**](ClusterBackup.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.cluster import Cluster

# TODO update the JSON string below
json = "{}"
# create an instance of Cluster from a JSON string
cluster_instance = Cluster.from_json(json)
# print the JSON string representation of the object
print(Cluster.to_json())

# convert the object into a dict
cluster_dict = cluster_instance.to_dict()
# create an instance of Cluster from a dict
cluster_from_dict = Cluster.from_dict(cluster_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


