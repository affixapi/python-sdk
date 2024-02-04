# openapi_client.ManagementApi

All URIs are relative to *https://api.affixapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**client**](ManagementApi.md#client) | **GET** /2023-03-01/management/client | Client
[**disconnect**](ManagementApi.md#disconnect) | **POST** /2023-03-01/management/disconnect | Disconnect token
[**introspect**](ManagementApi.md#introspect) | **GET** /2023-03-01/management/introspect | Inspect token
[**token**](ManagementApi.md#token) | **POST** /2023-03-01/management/token | Create token
[**tokens**](ManagementApi.md#tokens) | **GET** /2023-03-01/management/tokens | Tokens
[**update_client**](ManagementApi.md#update_client) | **POST** /2023-03-01/management/client | Update client


# **client**
> ClientResponse client()

Client

View client attributes 

### Example

* Api Key Authentication (basic):
```python
import time
import openapi_client
from openapi_client.api import management_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.client_response import ClientResponse
from openapi_client.model.inline_response400 import InlineResponse400
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: basic
configuration.api_key['basic'] = 'YOUR_API_KEY'

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['basic'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = management_api.ManagementApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Client
        api_response = api_instance.client()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ManagementApi->client: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**ClientResponse**](ClientResponse.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**400** | Bad Request |  -  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disconnect**
> DisconnectResponse disconnect()

Disconnect token

Disconnect the token. A disconnected token will no longer return data. Data requests with a disconnected token will return a 403 Forbidden 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import management_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.disconnect_response import DisconnectResponse
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: access-token
configuration.api_key['access-token'] = 'YOUR_API_KEY'

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['access-token'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = management_api.ManagementApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Disconnect token
        api_response = api_instance.disconnect()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ManagementApi->disconnect: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**DisconnectResponse**](DisconnectResponse.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**403** | Forbidden |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **introspect**
> IntrospectResponse introspect()

Inspect token

Retrieve data about the token, such as `scopes`, `mode`, `provider`, and if it is active 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import management_api
from openapi_client.model.introspect_response import IntrospectResponse
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.id_and_message_response import IdAndMessageResponse
from openapi_client.model.inline_response400 import InlineResponse400
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: access-token
configuration.api_key['access-token'] = 'YOUR_API_KEY'

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['access-token'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = management_api.ManagementApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Inspect token
        api_response = api_instance.introspect()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ManagementApi->introspect: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**IntrospectResponse**](IntrospectResponse.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**400** | Bad Request |  -  |
**403** | Forbidden |  -  |
**404** | Not Found |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **token**
> TokenResponse token(token_request)

Create token

Exchange an `authorization_code` for an `access_token` after receiving on from the `redirect_uri` you specifiy after a successful user connection 

### Example

```python
import time
import openapi_client
from openapi_client.api import management_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.id_and_message_response import IdAndMessageResponse
from openapi_client.model.inline_response409 import InlineResponse409
from openapi_client.model.token_response import TokenResponse
from openapi_client.model.inline_response400 import InlineResponse400
from openapi_client.model.token_request import TokenRequest
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = management_api.ManagementApi(api_client)
    token_request = TokenRequest(
        client_id="00000000-00000000-00000000-00000000",
        client_secret="ffffffff-ffffffff-ffffffff-ffffffff",
        grant_type="authorization_code",
        code="Y2xpZW50IzkzMTU4MGQwLWYwYjctNGJiOC1iYmZmLWI4MTNlYzMxNTVjYXxjb2RlIzE1MmIwYjk3LTg2ZWMtNDZlNC1hZDUyLWY5ZTAxNzE2MDIwNAo=",
        redirect_uri="https://example.com",
    ) # TokenRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Create token
        api_response = api_instance.token(token_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ManagementApi->token: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_request** | [**TokenRequest**](TokenRequest.md)|  |

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Success |  -  |
**400** | Bad Request |  -  |
**404** | Not Found |  -  |
**409** | Not Found |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tokens**
> TokensResponse tokens()

Tokens

View tokens and token status for respective client 

### Example

* Api Key Authentication (basic):
```python
import time
import openapi_client
from openapi_client.api import management_api
from openapi_client.model.tokens_response import TokensResponse
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.id_and_message_response import IdAndMessageResponse
from openapi_client.model.inline_response409 import InlineResponse409
from openapi_client.model.inline_response400 import InlineResponse400
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: basic
configuration.api_key['basic'] = 'YOUR_API_KEY'

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['basic'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = management_api.ManagementApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Tokens
        api_response = api_instance.tokens()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ManagementApi->tokens: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**TokensResponse**](TokensResponse.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**400** | Bad Request |  -  |
**404** | Not Found |  -  |
**409** | Not Found |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_client**
> ClientResponse update_client(client_request)

Update client

Update attributes of the client.  Update the `name`, `client_secret`, or `webhook_uri` of the client 

### Example

* Api Key Authentication (basic):
```python
import time
import openapi_client
from openapi_client.api import management_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.inline_response409 import InlineResponse409
from openapi_client.model.client_response import ClientResponse
from openapi_client.model.inline_response400 import InlineResponse400
from openapi_client.model.client_request import ClientRequest
from pprint import pprint
# Defining the host is optional and defaults to https://api.affixapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.affixapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: basic
configuration.api_key['basic'] = 'YOUR_API_KEY'

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['basic'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = management_api.ManagementApi(api_client)
    client_request = ClientRequest(
        client_secret=["ffffffff-ffffffff-ffffffff-ffffffff","aaaaaaaa-aaaaaaaa-aaaaaaaa-aaaaaaaa"],
        redirect_uris=["https://app.your-company.com","https://dev.app.your-company.com"],
        name="Your App",
        webhook_uri="https://webhooks.your-company.com/aaaaaaaa-aaaaaaaa-aaaaaaaa-aaaaaaaa",
    ) # ClientRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Update client
        api_response = api_instance.update_client(client_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ManagementApi->update_client: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_request** | [**ClientRequest**](ClientRequest.md)|  |

### Return type

[**ClientResponse**](ClientResponse.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**400** | Bad Request |  -  |
**401** | Authentication Error |  -  |
**409** | Not Found |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

