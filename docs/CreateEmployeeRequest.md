# CreateEmployeeRequest


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first_name** | **str** | the first name of the individual | 
**last_name** | **str** | the last name of the individual | 
**employee_number** | **str, none_type** |  | [optional] 
**display_full_name** | **str, none_type** |  | [optional] 
**nationality** | **str, none_type** |  | [optional] 
**job_title** | **str, none_type** |  | [optional] 
**work_email** | **str, none_type** | the work email of the individual | [optional] 
**personal_email** | **str, none_type** | the personal email of the individual | [optional] 
**mobile_phone_number** | **str, none_type** | +1234567890 | [optional] 
**tax_id** | **str, none_type** |  | [optional] 
**gender** | **str, none_type** |  | [optional] 
**ethnicity** | **str, none_type** |  | [optional] 
**marital_status** | **str, none_type** | &#x60;other&#x60; option can include co-habitating, civil partnership, separated, widowed, etc  | [optional] 
**date_of_birth** | **date, none_type** |  | [optional] 
**employment_status** | [**EmploymentStatusNotNullRequest**](EmploymentStatusNotNullRequest.md) |  | [optional] 
**employment_type** | **str, none_type** |  | [optional] 
**start_date** | **date, none_type** |  | [optional] 
**termination_date** | **date, none_type** |  | [optional] 
**avatar** | **str, none_type** |  | [optional] 
**home_location** | [**AddressNoNonNullRequest**](AddressNoNonNullRequest.md) |  | [optional] 
**work_location** | [**LocationNoNonNullRequest**](LocationNoNonNullRequest.md) |  | [optional] 
**manager** | [**CreateEmployeeRequestManager**](CreateEmployeeRequestManager.md) |  | [optional] 
**bank_account** | [**CreateEmployeeRequestBankAccount**](CreateEmployeeRequestBankAccount.md) |  | [optional] 
**employment_history** | [**[EmploymentHistoryNoNonNullRequest], none_type**](EmploymentHistoryNoNonNullRequest.md) |  | [optional] 
**compensation_history** | [**[CompensationHistoryNoNonNullRequest], none_type**](CompensationHistoryNoNonNullRequest.md) |  | [optional] 
**custom_fields** | **{str: (bool, date, datetime, dict, float, int, list, str, none_type)}, none_type** |  | [optional] 
**groups** | [**GroupsNoNullEnumRequest**](GroupsNoNullEnumRequest.md) |  | [optional] 
**dependents** | [**[CreateEmployeeRequestDependents], none_type**](CreateEmployeeRequestDependents.md) |  | [optional] 
**emergency_contacts** | [**[CreateEmployeeRequestEmergencyContacts], none_type**](CreateEmployeeRequestEmergencyContacts.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


