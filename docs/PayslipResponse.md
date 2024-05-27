# PayslipResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str, none_type** | The Affix-assigned id of the payslip | 
**remote_id** | **str, none_type** | the remote system-assigned id of the payrun | 
**employee_id** | **str** |  | 
**employee_remote_id** | **str** |  | 
**payrun_id** | **str** |  | 
**payrun_remote_id** | **str** |  | 
**payrun_type** | [**PayrunTypeResponse**](PayrunTypeResponse.md) |  | 
**currency** | [**CurrencyNotNullResponse**](CurrencyNotNullResponse.md) |  | 
**gross_pay** | **float, none_type** | if USD/EUR/GBP, in cent | 
**net_pay** | **float, none_type** | if USD/EUR/GBP, in cent | 
**start_date** | **date** |  | 
**end_date** | **date** |  | 
**payment_date** | **date** |  | 
**earnings** | [**[PayslipResponseEarnings], none_type**](PayslipResponseEarnings.md) |  | 
**contributions** | [**[PayslipResponseContributions], none_type**](PayslipResponseContributions.md) | Items paid by the employer that are not included in gross pay, such as employer-paid portion of private health insurance  | 
**deductions** | [**[PayslipResponseDeductions], none_type**](PayslipResponseDeductions.md) |  | 
**taxes** | [**[PayslipResponseTaxes], none_type**](PayslipResponseTaxes.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


