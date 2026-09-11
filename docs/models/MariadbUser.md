# MariadbUser

Credentials for the initial database user to be created.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **str** | The username of the initial MariaDB user. Must be 16 characters or less and must include only alphanumeric characters (&#x60;[A-Za-z0-9_]&#x60;) and underscores (&#x60;_&#x60;). Some usernames are reserved for platform use (for example &#x60;mariadb&#x60;, &#x60;admin&#x60;, &#x60;standby&#x60;).  | 
**password** | **str** | The password for the initial MariaDB user. Must be between 10 and 256 characters long. For a strong password we recommend that it also meets the following criteria, though these are not enforced: - Contains at least one lowercase letter. - Contains at least one uppercase letter. - Contains at least one digit (0-9). - Contains at least one special character from the set: @$!%*?&amp;  | 
**database** | **str** | The name of the initial database to be created. Must be 63 characters or less and must include only alphanumeric characters (&#x60;[a-z0-9A-Z]&#x60;) and underscores (&#x60;_&#x60;).  | 

## Example

```python
from ionoscloud_dbaas_mariadb.models.mariadb_user import MariadbUser

# TODO update the JSON string below
json = "{}"
# create an instance of MariadbUser from a JSON string
mariadb_user_instance = MariadbUser.from_json(json)
# print the JSON string representation of the object
print(MariadbUser.to_json())

# convert the object into a dict
mariadb_user_dict = mariadb_user_instance.to_dict()
# create an instance of MariadbUser from a dict
mariadb_user_from_dict = MariadbUser.from_dict(mariadb_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


