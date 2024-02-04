# openapi_client.CoreApi

All URIs are relative to *https://api.affixapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**providers**](CoreApi.md#providers) | **GET** /providers | Providers


# **providers**
> ProvidersResponse providers()

Providers

Retrieve the api modes (official, developer) and providers for the respective modes 

### Example

```python
import time
import openapi_client
from openapi_client.api import core_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.providers_response import ProvidersResponse
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = core_api.CoreApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Providers
        api_response = api_instance.providers()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling CoreApi->providers: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**ProvidersResponse**](ProvidersResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

