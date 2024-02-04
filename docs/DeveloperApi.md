# openapi_client.DeveloperApi

All URIs are relative to *https://api.affixapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**developer_companies20230301**](DeveloperApi.md#developer_companies20230301) | **GET** /2023-03-01/developer/company | Company
[**developer_create_employee20230301**](DeveloperApi.md#developer_create_employee20230301) | **POST** /2023-03-01/developer/employee | Create employee
[**developer_employees20230301**](DeveloperApi.md#developer_employees20230301) | **GET** /2023-03-01/developer/employees | Employees
[**developer_groups20230301**](DeveloperApi.md#developer_groups20230301) | **GET** /2023-03-01/developer/groups | Groups
[**developer_identity20230301**](DeveloperApi.md#developer_identity20230301) | **GET** /2023-03-01/developer/identity | Identity
[**developer_payruns20230301**](DeveloperApi.md#developer_payruns20230301) | **GET** /2023-03-01/developer/payruns | Payruns
[**developer_payslips20230301**](DeveloperApi.md#developer_payslips20230301) | **GET** /2023-03-01/developer/payruns/{payrun_id} | Payslips
[**developer_time_off_balances20230301**](DeveloperApi.md#developer_time_off_balances20230301) | **GET** /2023-03-01/developer/time-off-balances | Time off balances
[**developer_time_off_entries20230301**](DeveloperApi.md#developer_time_off_entries20230301) | **GET** /2023-03-01/developer/time-off-entries | Time off entries
[**developer_timesheets20230301**](DeveloperApi.md#developer_timesheets20230301) | **GET** /2023-03-01/developer/timesheets | Timesheets
[**developer_work_locations20230301**](DeveloperApi.md#developer_work_locations20230301) | **GET** /2023-03-01/developer/work-locations | Work locations


# **developer_companies20230301**
> Companies20230301Response developer_companies20230301()

Company

Retrieve company information 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Company
        api_response = api_instance.developer_companies20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_companies20230301: %s\n" % e)
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

# **developer_create_employee20230301**
> EmployeeResponse developer_create_employee20230301(create_employee_request)

Create employee

Creates a new Employee 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
from openapi_client.model.employee_response import EmployeeResponse
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.create_employee_request import CreateEmployeeRequest
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
    api_instance = developer_api.DeveloperApi(api_client)
    create_employee_request = CreateEmployeeRequest(
        employee_number="2",
        first_name="Greg",
        last_name="Hirsch",
        display_full_name="Hirsch",
        nationality="Irish",
        job_title="Software developer",
        work_email="greg@affixapi.com",
        personal_email="greg@gmail.com",
        mobile_phone_number="Hirsch",
        tax_id="1234567890",
        gender="male",
        ethnicity="white",
        marital_status="single",
        date_of_birth=dateutil_parser('Sat Nov 10 00:00:00 UTC 1990').date(),
        employment_status="active",
        employment_type="full_time",
        start_date=dateutil_parser('Sun Oct 11 00:00:00 UTC 2020').date(),
        termination_date=dateutil_parser('Tue Oct 12 00:00:00 UTC 2021').date(),
        avatar="http://alturl.com/h2h8m",
        home_location=AddressNoNonNullRequest(
            street_address="221 S Main Street",
            locality="Yuma",
            administrative_area="AZ",
            country="IE",
            post_code="30691",
        ),
        work_location=LocationNoNonNullRequest(
            id="cD0yMDIxLTAxLTA2KzAzJTNBMjQlM0E1My40MzQzMjYlMkIwMCUzQTAw",
            remote_id="19202938",
            name="NYC Office",
            type="office",
            address=AddressNoNonNullRequest(
                street_address="221 S Main Street",
                locality="Yuma",
                administrative_area="AZ",
                country="IE",
                post_code="30691",
            ),
        ),
        manager=CreateEmployeeRequestManager(
            first_name="first_name_example",
            last_name="last_name_example",
            id="id_example",
            work_email="work_email_example",
            remote_id="remote_id_example",
        ),
        bank_account=CreateEmployeeRequestBankAccount(
            account_number="account_number_example",
            bank_name="bank_name_example",
            bic="bic_example",
            holder_name="holder_name_example",
            iban="iban_example",
        ),
        employments=[
            EmploymentNoNullEnumRequest(
                job_title="Software Developer",
                pay_rate=85000,
                pay_period="year",
                pay_frequency="semimonthly",
                employment_type="full_time",
                currency=CurrencyRequest("usd"),
                effective_date=dateutil_parser('Sun Oct 11 00:00:00 UTC 2020').date(),
            ),
        ],
        custom_fields={},
        groups=GroupsNoNullEnumRequest([
            GroupNoNullEnumRequest(
                id="4B9bKBpX5tnwjiG93TAqF7ci",
                remote_id="49",
                name="Customer Success",
                type="TEAM",
            ),
        ]),
    ) # CreateEmployeeRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Create employee
        api_response = api_instance.developer_create_employee20230301(create_employee_request)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_create_employee20230301: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_employee_request** | [**CreateEmployeeRequest**](CreateEmployeeRequest.md)|  |

### Return type

[**EmployeeResponse**](EmployeeResponse.md)

### Authorization

[access-token](../README.md#access-token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Success |  -  |
**400** | Bad Request |  -  |
**429** | Rate Limited / Too Many Requests |  * Retry-After - Retry your call after the specified amount of seconds <br>  |
**500** | Server Error |  -  |
**501** | Not Implemented |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **developer_employees20230301**
> Employees20230301Response developer_employees20230301()

Employees

List the individuals (employees, contractors, accountants, and others) listed in the HRIS/Payroll software 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
from openapi_client.model.message_response import MessageResponse
from openapi_client.model.employees20230301_response import Employees20230301Response
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Employees
        api_response = api_instance.developer_employees20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_employees20230301: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

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

# **developer_groups20230301**
> Groups20230301Response developer_groups20230301()

Groups

The Group object is used to represent any subset of employees, such as PayGroup, Team, or Department. Employees can be in multiple Groups. 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Groups
        api_response = api_instance.developer_groups20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_groups20230301: %s\n" % e)
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

# **developer_identity20230301**
> IdentityResponse developer_identity20230301()

Identity

List information of the user for the respective account 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Identity
        api_response = api_instance.developer_identity20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_identity20230301: %s\n" % e)
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

# **developer_payruns20230301**
> Payruns20230301Response developer_payruns20230301(start_date, end_date)

Payruns

List all the pay runs that occurred during the respective period.  Supported integrations:   - sageone   - simplepay.ie   - brightpay connect 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)
    start_date = dateutil_parser('Fri Jan 01 00:00:00 UTC 2021').date() # date | The start date of the search period
    end_date = dateutil_parser('Fri Dec 31 00:00:00 UTC 2021').date() # date | The end date of the search period

    # example passing only required values which don't have defaults set
    try:
        # Payruns
        api_response = api_instance.developer_payruns20230301(start_date, end_date)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_payruns20230301: %s\n" % e)
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

# **developer_payslips20230301**
> Payslips20230301Response developer_payslips20230301(payrun_id)

Payslips

Retrieves payslips from a specific payrun.  Supported integrations:   - sageone   - simplepay.ie   - brightpay connect 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)
    payrun_id = "payrun_id_example" # str | The id of the payrun.

    # example passing only required values which don't have defaults set
    try:
        # Payslips
        api_response = api_instance.developer_payslips20230301(payrun_id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_payslips20230301: %s\n" % e)
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

# **developer_time_off_balances20230301**
> TimeOffBalances20230301Response developer_time_off_balances20230301()

Time off balances

Retrieve all time off balances. 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Time off balances
        api_response = api_instance.developer_time_off_balances20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_time_off_balances20230301: %s\n" % e)
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

# **developer_time_off_entries20230301**
> TimeOffEntries20230301Response developer_time_off_entries20230301()

Time off entries

Retrieve time off / absence entries 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Time off entries
        api_response = api_instance.developer_time_off_entries20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_time_off_entries20230301: %s\n" % e)
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

# **developer_timesheets20230301**
> Timesheets20230301Response developer_timesheets20230301()

Timesheets

Retrieve Timesheets 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Timesheets
        api_response = api_instance.developer_timesheets20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_timesheets20230301: %s\n" % e)
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

# **developer_work_locations20230301**
> WorkLocations20230301Response developer_work_locations20230301()

Work locations

The Location object is used to represent an address that can be associated with an employee 

### Example

* Api Key Authentication (access-token):
```python
import time
import openapi_client
from openapi_client.api import developer_api
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
    api_instance = developer_api.DeveloperApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Work locations
        api_response = api_instance.developer_work_locations20230301()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling DeveloperApi->developer_work_locations20230301: %s\n" % e)
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

