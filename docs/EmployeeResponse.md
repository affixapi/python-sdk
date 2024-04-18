# EmployeeResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The Affix-assigned id of the individual | [readonly] 
**remote_id** | **str** | the remote system-assigned id of the individual | [readonly] 
**employee_number** | **str, none_type** |  | 
**first_name** | **str** | the first name of the individual | 
**last_name** | **str** | the last name of the individual | 
**display_full_name** | **str, none_type** |  | 
**nationality** | **str, none_type** |  | 
**job_title** | **str, none_type** |  | 
**work_email** | **str, none_type** | the work email of the individual | 
**personal_email** | **str, none_type** | the personal email of the individual | 
**mobile_phone_number** | **str, none_type** | +1234567890 | 
**tax_id** | **str, none_type** |  | 
**gender** | **str, none_type** |  | 
**ethnicity** | **str, none_type** |  | 
**marital_status** | **str, none_type** | &#x60;other&#x60; option can include co-habitating, civil partnership, separated, divorced, widowed, etc  | 
**date_of_birth** | **date, none_type** |  | 
**employment_status** | **str, none_type** |  | 
**employment_type** | **str, none_type** |  | 
**start_date** | **date, none_type** |  | 
**remote_created_at** | **date, none_type** |  | [readonly] 
**termination_date** | **date, none_type** |  | 
**avatar** | **str, none_type** |  | 
**home_location** | [**AddressResponse**](AddressResponse.md) |  | 
**work_location** | [**LocationResponse**](LocationResponse.md) |  | 
**manager** | [**EmployeeResponseManager**](EmployeeResponseManager.md) |  | 
**bank_account** | [**CreateEmployeeRequestBankAccount**](CreateEmployeeRequestBankAccount.md) |  | 
**employments** | [**[EmploymentResponse], none_type**](EmploymentResponse.md) |  | 
**custom_fields** | **{str: (bool, date, datetime, dict, float, int, list, str, none_type)}, none_type** |  | 
**groups** | [**Groups20230301Response**](Groups20230301Response.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


