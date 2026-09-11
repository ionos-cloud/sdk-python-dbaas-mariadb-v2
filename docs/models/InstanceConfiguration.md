# InstanceConfiguration


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** | The total number of instances in the cluster. A value of 1 creates a single-instance cluster. Values from 2 to 5 create a replicated cluster with one primary and n-1 secondary instances.  | 
**ram** | **int** | The amount of memory (RAM) per instance in gigabytes (GB). On update, RAM can be increased or decreased. | 
**cores** | **int** | The number of CPU cores per instance. On update, cores can be increased or decreased. | 
**storage_size** | **int** | The amount of storage per instance in gigabytes (GB). On update, storage size can only be increased; it cannot be reduced.  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.instance_configuration import InstanceConfiguration

# TODO update the JSON string below
json = "{}"
# create an instance of InstanceConfiguration from a JSON string
instance_configuration_instance = InstanceConfiguration.from_json(json)
# print the JSON string representation of the object
print(InstanceConfiguration.to_json())

# convert the object into a dict
instance_configuration_dict = instance_configuration_instance.to_dict()
# create an instance of InstanceConfiguration from a dict
instance_configuration_from_dict = InstanceConfiguration.from_dict(instance_configuration_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


