# ionoscloud_dbaas_mariadb.BackupsApi

All URIs are relative to *https://mariadb.de-txl.ionos.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**backups_find_by_id**](BackupsApi.md#backups_find_by_id) | **GET** /backups/{backupId} | Retrieve Backup
[**backups_get**](BackupsApi.md#backups_get) | **GET** /backups | Retrieve all Backups


# **backups_find_by_id**
> BackupRead backups_find_by_id(backup_id)

Retrieve Backup

Returns the Backup by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.backup_read import BackupRead
from ionoscloud_dbaas_mariadb.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://mariadb.de-txl.ionos.com/v2
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_dbaas_mariadb.Configuration(
    host = "https://mariadb.de-txl.ionos.com/v2"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_dbaas_mariadb.Configuration(
    token = os.environ["IONOS_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_dbaas_mariadb.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_dbaas_mariadb.BackupsApi(api_client)
    backup_id = '45ca67fb-8b07-5783-9c97-2d35acceb084' # str | The ID (UUID) of the Backup.

    try:
        # Retrieve Backup
        api_response = api_instance.backups_find_by_id(backup_id)
        print("The response of BackupsApi->backups_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupsApi->backups_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **backup_id** | **str**| The ID (UUID) of the Backup. | 

### Return type

[**BackupRead**](BackupRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting Backup was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **backups_get**
> BackupReadList backups_get(offset=offset, limit=limit, filter_cluster_id=filter_cluster_id)

Retrieve all Backups

This endpoint enables retrieving all Backups using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.backup_read_list import BackupReadList
from ionoscloud_dbaas_mariadb.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://mariadb.de-txl.ionos.com/v2
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_dbaas_mariadb.Configuration(
    host = "https://mariadb.de-txl.ionos.com/v2"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_dbaas_mariadb.Configuration(
    token = os.environ["IONOS_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_dbaas_mariadb.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_dbaas_mariadb.BackupsApi(api_client)
    offset = 0 # int | The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. (optional) (default to 0)
    limit = 100 # int | The maximum number of elements to return. Use this parameter together with the offset for pagination. (optional) (default to 100)
    filter_cluster_id = 'filter_cluster_id_example' # str | The ID (UUID) of the cluster to filter backups by. (optional)

    try:
        # Retrieve all Backups
        api_response = api_instance.backups_get(offset=offset, limit=limit, filter_cluster_id=filter_cluster_id)
        print("The response of BackupsApi->backups_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupsApi->backups_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. | [optional] [default to 0]
 **limit** | **int**| The maximum number of elements to return. Use this parameter together with the offset for pagination. | [optional] [default to 100]
 **filter_cluster_id** | **str**| The ID (UUID) of the cluster to filter backups by. | [optional] 

### Return type

[**BackupReadList**](BackupReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Backups successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

