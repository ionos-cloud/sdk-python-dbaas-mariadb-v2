# MariadbVersionRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the MariadbVersion. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the MariadbVersion. | 
**metadata** | **object** |  | [readonly] 
**properties** | [**MariadbVersion**](MariadbVersion.md) |  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.mariadb_version_read import MariadbVersionRead

# TODO update the JSON string below
json = "{}"
# create an instance of MariadbVersionRead from a JSON string
mariadb_version_read_instance = MariadbVersionRead.from_json(json)
# print the JSON string representation of the object
print(MariadbVersionRead.to_json())

# convert the object into a dict
mariadb_version_read_dict = mariadb_version_read_instance.to_dict()
# create an instance of MariadbVersionRead from a dict
mariadb_version_read_from_dict = MariadbVersionRead.from_dict(mariadb_version_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


