# ionoscloud_dbaas_mariadb.BackupLocationsApi

All URIs are relative to *https://mariadb.de-txl.ionos.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**backuplocations_find_by_id**](BackupLocationsApi.md#backuplocations_find_by_id) | **GET** /backup-locations/{backupLocationId} | Retrieve BackupLocation
[**backuplocations_get**](BackupLocationsApi.md#backuplocations_get) | **GET** /backup-locations | Retrieve all BackupLocations


# **backuplocations_find_by_id**
> BackupLocationRead backuplocations_find_by_id(backup_location_id)

Retrieve BackupLocation

Returns the BackupLocation by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.backup_location_read import BackupLocationRead
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
    api_instance = ionoscloud_dbaas_mariadb.BackupLocationsApi(api_client)
    backup_location_id = '7fa1dd11-59dd-53a5-ab67-50f649c8e3eb' # str | The ID (UUID) of the BackupLocation.

    try:
        # Retrieve BackupLocation
        api_response = api_instance.backuplocations_find_by_id(backup_location_id)
        print("The response of BackupLocationsApi->backuplocations_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupLocationsApi->backuplocations_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **backup_location_id** | **str**| The ID (UUID) of the BackupLocation. | 

### Return type

[**BackupLocationRead**](BackupLocationRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting BackupLocation was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **backuplocations_get**
> BackupLocationReadList backuplocations_get(offset=offset, limit=limit)

Retrieve all BackupLocations

This endpoint enables retrieving all BackupLocations using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.backup_location_read_list import BackupLocationReadList
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
    api_instance = ionoscloud_dbaas_mariadb.BackupLocationsApi(api_client)
    offset = 0 # int | The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. (optional) (default to 0)
    limit = 100 # int | The maximum number of elements to return. Use this parameter together with the offset for pagination. (optional) (default to 100)

    try:
        # Retrieve all BackupLocations
        api_response = api_instance.backuplocations_get(offset=offset, limit=limit)
        print("The response of BackupLocationsApi->backuplocations_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupLocationsApi->backuplocations_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. | [optional] [default to 0]
 **limit** | **int**| The maximum number of elements to return. Use this parameter together with the offset for pagination. | [optional] [default to 100]

### Return type

[**BackupLocationReadList**](BackupLocationReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested BackupLocations successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

