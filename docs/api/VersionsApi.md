# ionoscloud_dbaas_mariadb.VersionsApi

All URIs are relative to *https://mariadb.de-txl.ionos.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**versions_find_by_id**](VersionsApi.md#versions_find_by_id) | **GET** /versions/{versionId} | Retrieve MariadbVersion
[**versions_get**](VersionsApi.md#versions_get) | **GET** /versions | Retrieve all Versions


# **versions_find_by_id**
> MariadbVersionRead versions_find_by_id(version_id)

Retrieve MariadbVersion

Returns the MariadbVersion by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.mariadb_version_read import MariadbVersionRead
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
    api_instance = ionoscloud_dbaas_mariadb.VersionsApi(api_client)
    version_id = '28620dce-018a-5818-a827-aea8fbc8c1cf' # str | The ID (UUID) of the MariadbVersion.

    try:
        # Retrieve MariadbVersion
        api_response = api_instance.versions_find_by_id(version_id)
        print("The response of VersionsApi->versions_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VersionsApi->versions_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **version_id** | **str**| The ID (UUID) of the MariadbVersion. | 

### Return type

[**MariadbVersionRead**](MariadbVersionRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting MariadbVersion was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **versions_get**
> MariadbVersionReadList versions_get(offset=offset, limit=limit)

Retrieve all Versions

This endpoint enables retrieving all Versions using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.mariadb_version_read_list import MariadbVersionReadList
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
    api_instance = ionoscloud_dbaas_mariadb.VersionsApi(api_client)
    offset = 0 # int | The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. (optional) (default to 0)
    limit = 100 # int | The maximum number of elements to return. Use this parameter together with the offset for pagination. (optional) (default to 100)

    try:
        # Retrieve all Versions
        api_response = api_instance.versions_get(offset=offset, limit=limit)
        print("The response of VersionsApi->versions_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VersionsApi->versions_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. | [optional] [default to 0]
 **limit** | **int**| The maximum number of elements to return. Use this parameter together with the offset for pagination. | [optional] [default to 100]

### Return type

[**MariadbVersionReadList**](MariadbVersionReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Versions successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

