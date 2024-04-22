# openapi_client.XHRVerticallyIntegratedApi

All URIs are relative to *https://api.affixapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**xhr_companies20230301**](XHRVerticallyIntegratedApi.md#xhr_companies20230301) | **GET** /2023-03-01/xhr/company | Company
[**xhr_employees20230301**](XHRVerticallyIntegratedApi.md#xhr_employees20230301) | **GET** /2023-03-01/xhr/employees | Employees
[**xhr_groups20230301**](XHRVerticallyIntegratedApi.md#xhr_groups20230301) | **GET** /2023-03-01/xhr/groups | Groups
[**xhr_identity20230301**](XHRVerticallyIntegratedApi.md#xhr_identity20230301) | **GET** /2023-03-01/xhr/identity | Identity
[**xhr_payruns20230301**](XHRVerticallyIntegratedApi.md#xhr_payruns20230301) | **GET** /2023-03-01/xhr/payruns | Payruns
[**xhr_payslips20230301**](XHRVerticallyIntegratedApi.md#xhr_payslips20230301) | **GET** /2023-03-01/xhr/payruns/{payrun_id} | Payslips
[**xhr_time_off_balances20230301**](XHRVerticallyIntegratedApi.md#xhr_time_off_balances20230301) | **GET** /2023-03-01/xhr/time-off-balances | Time off balances
[**xhr_time_off_entries20230301**](XHRVerticallyIntegratedApi.md#xhr_time_off_entries20230301) | **GET** /2023-03-01/xhr/time-off-entries | Time off entries
[**xhr_timesheets20230301**](XHRVerticallyIntegratedApi.md#xhr_timesheets20230301) | **GET** /2023-03-01/xhr/timesheets | Timesheets
[**xhr_work_locations20230301**](XHRVerticallyIntegratedApi.md#xhr_work_locations20230301) | **GET** /2023-03-01/xhr/work-locations | Work locations


# **xhr_companies20230301**
> Companies20230301Response xhr_companies20230301()

Company

Retrieve company information 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.companies20230301_response import Companies20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Company
        api_response = api_instance.xhr_companies20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_companies20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**Companies20230301Response**](Companies20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_employees20230301**
> Employees20230301Response xhr_employees20230301()

Employees

List the individuals (employees, contractors, accountants, and others) listed in the HRIS/Payroll software 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.employees20230301_response import Employees20230301Response
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.employment_status import EmploymentStatus
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)
    employment_status = EmploymentStatus("active") # EmploymentStatus | Enable server-side filtering of the `employment_status` attribute  (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Employees
        api_response = api_instance.xhr_employees20230301(employment_status=employment_status)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_employees20230301: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employment_status** | **EmploymentStatus**| Enable server-side filtering of the &#x60;employment_status&#x60; attribute  | [optional]

### Return type

[**Employees20230301Response**](Employees20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_groups20230301**
> Groups20230301Response xhr_groups20230301()

Groups

The Group object is used to represent any subset of employees, such as PayGroup, Team, or Department. Employees can be in multiple Groups. 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.groups20230301_response import Groups20230301Response
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Groups
        api_response = api_instance.xhr_groups20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_groups20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**Groups20230301Response**](Groups20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_identity20230301**
> IdentityResponse xhr_identity20230301()

Identity

List information of the user for the respective account 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.identity_response import IdentityResponse
from openapi_client.model.inline_response401 import InlineResponse401
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Identity
        api_response = api_instance.xhr_identity20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_identity20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**IdentityResponse**](IdentityResponse.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_payruns20230301**
> Payruns20230301Response xhr_payruns20230301(start_date, end_date)

Payruns

List all the pay runs that occurred during the respective period.  Supported integrations:   - brain payroll   - brightpay connect   - deel   - gusto   - justworks   - moorepay   - onpay   - oyster   - parolla.ie   - paycircle   - payfit   - pento.io   - quickbooks online   - remote.com   - rippling   - sageone   - shape payroll   - simplepay.ie   - staffology   - xero uk 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.payruns20230301_response import Payruns20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)
    start_date = dateutil_parser('Fri Jan 01 00:00:00 UTC 2021').date() # date | The start date of the search period
    end_date = dateutil_parser('Fri Dec 31 00:00:00 UTC 2021').date() # date | The end date of the search period

    # example passing only required values which don't have defaults set
    try:
        # Payruns
        api_response = api_instance.xhr_payruns20230301(start_date, end_date)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_payruns20230301: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **date**| The start date of the search period |
 **end_date** | **date**| The end date of the search period |

### Return type

[**Payruns20230301Response**](Payruns20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_payslips20230301**
> Payslips20230301Response xhr_payslips20230301(payrun_id)

Payslips

Retrieves payslips from a specific payrun.  Supported integrations:   - sageone   - simplepay.ie   - brightpay connect 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.payslips20230301_response import Payslips20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)
    payrun_id = "payrun_id_example" # str | The id of the payrun.

    # example passing only required values which don't have defaults set
    try:
        # Payslips
        api_response = api_instance.xhr_payslips20230301(payrun_id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_payslips20230301: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payrun_id** | **str**| The id of the payrun. |

### Return type

[**Payslips20230301Response**](Payslips20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_time_off_balances20230301**
> TimeOffBalances20230301Response xhr_time_off_balances20230301()

Time off balances

Retrieve all time off balances. 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.time_off_balances20230301_response import TimeOffBalances20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Time off balances
        api_response = api_instance.xhr_time_off_balances20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_time_off_balances20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**TimeOffBalances20230301Response**](TimeOffBalances20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_time_off_entries20230301**
> TimeOffEntries20230301Response xhr_time_off_entries20230301()

Time off entries

Retrieve time off / absence entries 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.time_off_entries20230301_response import TimeOffEntries20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Time off entries
        api_response = api_instance.xhr_time_off_entries20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_time_off_entries20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**TimeOffEntries20230301Response**](TimeOffEntries20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_timesheets20230301**
> Timesheets20230301Response xhr_timesheets20230301()

Timesheets

Retrieve Timesheets 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.timesheets20230301_response import Timesheets20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Timesheets
        api_response = api_instance.xhr_timesheets20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_timesheets20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**Timesheets20230301Response**](Timesheets20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **xhr_work_locations20230301**
> WorkLocations20230301Response xhr_work_locations20230301()

Work locations

The Location object is used to represent an address that can be associated with an employee 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import xhr__vertically_integrated_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.inline_response401 import InlineResponse401
from openapi_client.model.work_locations20230301_response import WorkLocations20230301Response
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
    api_instance = xhr__vertically_integrated_api.XHRVerticallyIntegratedApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Work locations
        api_response = api_instance.xhr_work_locations20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling XHRVerticallyIntegratedApi->xhr_work_locations20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**WorkLocations20230301Response**](WorkLocations20230301Response.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**202** | Accepted + pending (async job started) |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**401** | Authentication Error |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

