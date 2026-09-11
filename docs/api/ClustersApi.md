# ionoscloud_dbaas_mariadb.ClustersApi

All URIs are relative to *https://mariadb.de-txl.ionos.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clusters_delete**](ClustersApi.md#clusters_delete) | **DELETE** /clusters/{clusterId} | Delete Cluster
[**clusters_find_by_id**](ClustersApi.md#clusters_find_by_id) | **GET** /clusters/{clusterId} | Retrieve Cluster
[**clusters_get**](ClustersApi.md#clusters_get) | **GET** /clusters | Retrieve all Clusters
[**clusters_post**](ClustersApi.md#clusters_post) | **POST** /clusters | Create Cluster
[**clusters_put**](ClustersApi.md#clusters_put) | **PUT** /clusters/{clusterId} | Ensure Cluster


# **clusters_delete**
> clusters_delete(cluster_id)

Delete Cluster

Deletes the specified Cluster.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
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
    api_instance = ionoscloud_dbaas_mariadb.ClustersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the Cluster.

    try:
        # Delete Cluster
        api_instance.clusters_delete(cluster_id)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the Cluster. | 

### Return type

void (empty response body)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Deleting Cluster was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_find_by_id**
> ClusterRead clusters_find_by_id(cluster_id)

Retrieve Cluster

Returns the Cluster by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.cluster_read import ClusterRead
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
    api_instance = ionoscloud_dbaas_mariadb.ClustersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the Cluster.

    try:
        # Retrieve Cluster
        api_response = api_instance.clusters_find_by_id(cluster_id)
        print("The response of ClustersApi->clusters_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the Cluster. | 

### Return type

[**ClusterRead**](ClusterRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting Cluster was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_get**
> ClusterReadList clusters_get(offset=offset, limit=limit, filter_name=filter_name, filter_state=filter_state)

Retrieve all Clusters

This endpoint enables retrieving all Clusters using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.cluster_read_list import ClusterReadList
from ionoscloud_dbaas_mariadb.models.mariadb_cluster_states import MariadbClusterStates
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
    api_instance = ionoscloud_dbaas_mariadb.ClustersApi(api_client)
    offset = 0 # int | The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. (optional) (default to 0)
    limit = 100 # int | The maximum number of elements to return. Use this parameter together with the offset for pagination. (optional) (default to 100)
    filter_name = 'filter_name_example' # str | The name used to filter clusters. Returns only clusters whose name contains the provided string. (optional)
    filter_state = ionoscloud_dbaas_mariadb.MariadbClusterStates() # MariadbClusterStates | Filters resources by state. If omitted, returns clusters in all states. (optional)

    try:
        # Retrieve all Clusters
        api_response = api_instance.clusters_get(offset=offset, limit=limit, filter_name=filter_name, filter_state=filter_state)
        print("The response of ClustersApi->clusters_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The first element (of the total list of elements) to include in the response. Use this parameter together with the limit for pagination. | [optional] [default to 0]
 **limit** | **int**| The maximum number of elements to return. Use this parameter together with the offset for pagination. | [optional] [default to 100]
 **filter_name** | **str**| The name used to filter clusters. Returns only clusters whose name contains the provided string. | [optional] 
 **filter_state** | [**MariadbClusterStates**](.md)| Filters resources by state. If omitted, returns clusters in all states. | [optional] 

### Return type

[**ClusterReadList**](ClusterReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Clusters successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_post**
> ClusterRead clusters_post(cluster_create)

Create Cluster

Creates a new Cluster.
The full Cluster needs to be provided to create the object.
Optional data will be filled with defaults or left empty.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.cluster_create import ClusterCreate
from ionoscloud_dbaas_mariadb.models.cluster_read import ClusterRead
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
    api_instance = ionoscloud_dbaas_mariadb.ClustersApi(api_client)
    cluster_create = ionoscloud_dbaas_mariadb.ClusterCreate() # ClusterCreate | Cluster to create.

    try:
        # Create Cluster
        api_response = api_instance.clusters_post(cluster_create)
        print("The response of ClustersApi->clusters_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_create** | [**ClusterCreate**](ClusterCreate.md)| Cluster to create. | 

### Return type

[**ClusterRead**](ClusterRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Cluster successfully created. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**415** | ### Unsupported Media Type The request has an unsupported media type.  |  -  |
**422** | ### Unprocessable Entity The request was well-formed but was unable to be followed due to semantic errors.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clusters_put**
> ClusterRead clusters_put(cluster_id, cluster_ensure)

Ensure Cluster

Ensures that the Cluster with the provided ID is created or modified.
The full Cluster needs to be provided to ensure
(either update or create) the Cluster. Non present data will
only be filled with defaults or left empty, but not take
previous values into consideration.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_dbaas_mariadb
from ionoscloud_dbaas_mariadb.models.cluster_ensure import ClusterEnsure
from ionoscloud_dbaas_mariadb.models.cluster_read import ClusterRead
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
    api_instance = ionoscloud_dbaas_mariadb.ClustersApi(api_client)
    cluster_id = 'e69b22a5-8fee-56b1-b6fb-4a07e4205ead' # str | The ID (UUID) of the Cluster.
    cluster_ensure = ionoscloud_dbaas_mariadb.ClusterEnsure() # ClusterEnsure | update Cluster

    try:
        # Ensure Cluster
        api_response = api_instance.clusters_put(cluster_id, cluster_ensure)
        print("The response of ClustersApi->clusters_put:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClustersApi->clusters_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cluster_id** | **str**| The ID (UUID) of the Cluster. | 
 **cluster_ensure** | [**ClusterEnsure**](ClusterEnsure.md)| update Cluster | 

### Return type

[**ClusterRead**](ClusterRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Cluster successfully updated. |  -  |
**201** | Cluster successfully ensured. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**409** | ### Conflict The UUID is already taken by another party, follow the guides to generate UUIDs uniquely.  |  -  |
**415** | ### Unsupported Media Type The request has an unsupported media type.  |  -  |
**422** | ### Unprocessable Entity The request was well-formed but was unable to be followed due to semantic errors.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

