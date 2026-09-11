# MariadbVersionReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | The offset specified in the request (if none was specified, the default offset is 0).  | [readonly] 
**limit** | **int** | The limit specified in the request (if none was specified, use the endpoint&#39;s default pagination limit).  | [readonly] 
**links** | [**Links**](Links.md) |  | 
**id** | **str** | ID of the list of MariadbVersion resources. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the list of MariadbVersion resources. | 
**items** | [**list[MariadbVersionRead]**](MariadbVersionRead.md) | The list of MariadbVersion resources. | [optional] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.mariadb_version_read_list import MariadbVersionReadList

# TODO update the JSON string below
json = "{}"
# create an instance of MariadbVersionReadList from a JSON string
mariadb_version_read_list_instance = MariadbVersionReadList.from_json(json)
# print the JSON string representation of the object
print(MariadbVersionReadList.to_json())

# convert the object into a dict
mariadb_version_read_list_dict = mariadb_version_read_list_instance.to_dict()
# create an instance of MariadbVersionReadList from a dict
mariadb_version_read_list_from_dict = MariadbVersionReadList.from_dict(mariadb_version_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


