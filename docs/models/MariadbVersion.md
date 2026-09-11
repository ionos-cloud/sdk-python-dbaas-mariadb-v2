# MariadbVersion

MariaDB version.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **str** | The MariaDB version for the cluster. Use GET /versions to retrieve the list of supported versions. To upgrade, provide a version listed in canUpgradeTo for the current version. Downgrades are not supported.  | [optional] 
**status** | **str** | The support status of the version. | [optional] 
**comment** | **str** | Additional information about the version status. | [optional] 
**can_upgrade_to** | **list[str]** | List of versions that a cluster running this version can be upgraded to. Only versions in this list are accepted when updating the version field via PUT.  | [optional] 

## Example

```python
from ionoscloud_dbaas_mariadb.models.mariadb_version import MariadbVersion

# TODO update the JSON string below
json = "{}"
# create an instance of MariadbVersion from a JSON string
mariadb_version_instance = MariadbVersion.from_json(json)
# print the JSON string representation of the object
print(MariadbVersion.to_json())

# convert the object into a dict
mariadb_version_dict = mariadb_version_instance.to_dict()
# create an instance of MariadbVersion from a dict
mariadb_version_from_dict = MariadbVersion.from_dict(mariadb_version_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


