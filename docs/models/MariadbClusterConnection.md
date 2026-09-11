# MariadbClusterConnection

Connection information of the MariaDB cluster. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**datacenter_id** | **str** | The data center to connect your instance to. | 
**lan_id** | **str** | The numeric LAN ID to connect your instance to. | 
**primary_instance_address** | **str** | Assigns the IP address and netmask to the cluster&#39;s primary instance, in CIDR notation. Note the following unavailable IP ranges: 10.208.0.0/12 10.233.0.0/18 10.233.64.0/18 192.168.230.0/24  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.mariadb_cluster_connection import MariadbClusterConnection

# TODO update the JSON string below
json = "{}"
# create an instance of MariadbClusterConnection from a JSON string
mariadb_cluster_connection_instance = MariadbClusterConnection.from_json(json)
# print the JSON string representation of the object
print(MariadbClusterConnection.to_json())

# convert the object into a dict
mariadb_cluster_connection_dict = mariadb_cluster_connection_instance.to_dict()
# create an instance of MariadbClusterConnection from a dict
mariadb_cluster_connection_from_dict = MariadbClusterConnection.from_dict(mariadb_cluster_connection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


